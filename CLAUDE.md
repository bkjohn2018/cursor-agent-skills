# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

A **portable distribution package** for a library of Cursor/agent skills and commands — not the live copy. Per `docs/sync-status.md`, the source of truth at runtime is `C:\Users\brian\.cursor\skills`, `.cursor\commands`, and `.cursor\skills-cursor`; this repo (`skills/`, `commands/`, `cursor-workflow-skills/`) is a synced snapshot meant for GitHub browsing and ZIP download to another machine (see `docs/install-from-zip.md`). There is no build, lint, or test tooling — every "skill" is plain Markdown with YAML frontmatter (`SKILL.md`), read directly by an agent harness.

**When editing here, remember you're editing the distribution copy, not the runtime one.** If the user is actively using these skills in Cursor/Claude Code day to day, the authoritative edit target is usually `.cursor/skills/<name>/SKILL.md`, and this repo needs a sync pass afterward (see `docs/sync-status.md`'s Sync Procedure) — don't assume a change here is live until it's copied back.

**Check `docs/handoff.md` first if resuming prior work** — it tracks open threads (currently: the `agents/` pilot's next validation step, and an Oracle 26B→26C content-readiness gap spanning this repo's sibling projects) so you don't have to re-derive context from scratch.

## Repository layout

```
skills/                 62 domain skills (finance, data governance, analytics, diagnostics, dashboards, documentation)
cursor-workflow-skills/ 13 meta-skills for creating skills/rules/hooks/subagents, unrelated to the domain content
commands/               13 Cursor slash commands, mostly thin orchestrators over skills/
agents/                 Subagents that delegate skills/commands across a team instead of one context
                        applying every chained skill. Pilot: governance-bundle-orchestrator + 3 specialists
                        + a QA gate, scoped to build-governance-bundle. Synced to .cursor/agents/ (verified).
legacy-agent-skills/    Older .agents/ copies retained for reference — do not treat as current
docs/                   inventory.md (categorized skill list), sync-status.md, install-from-zip.md
```

`docs/inventory.md` is the maintained category index — update it whenever a skill folder is added, removed, or renamed. `docs/sync-status.md` tracks counts and last-sync date — update both together.

## How skills are designed — read before adding or editing one

This library is not a flat toolbox; skills are deliberately composable pipeline stages, and new skills should follow the same conventions.

**1. Skills hand off to each other by name in their `description` field.** This is how the agent harness decides sequencing and avoids scope overlap. Existing examples: `"Use data-standards-management first when deciding data standard domains..."` (`policy-and-standard-writing`), `"Use internal-control-design for broader COSO-style control matrices... and data-quality-controls for data correctness monitoring"` (`data-quality-controls`). When adding a skill that overlaps an existing one, add the disambiguating cross-reference in both descriptions rather than letting them silently compete.

**2. Every skill anchors to a named external framework, never freelance methodology.** DAMA-DMBOK (data governance/management/quality skills), COSO (`internal-control-design`), ISO 9001 clause 7.5 (`finance-documentation-lifecycle`), Kimball + Hoberman (`dimensional-modeling`, `data-model-scorecard-review`), NIST AI RMF + NIST SP 800-53 (`finance-ai-risk-control-mapping`, `data-security-and-privacy-controls`), *Storytelling with Data* (`analytics-storytelling`). A new skill in an established area should say which framework it's aligned to in its own frontmatter description, not just describe behavior.

**3. Large deliverables are deliberately split into narrow single-purpose skills, not one broad skill.** E.g. a dashboard is 5 skills in sequence — `dashboard-product-framing` (why) → `dashboard-information-architecture` (structure) → `dashboard-metric-semantics` (meaning) → `governance-dashboard-content-model` (data shape) → `dashboard-frontend-implementation` (code) — so framing can't be skipped straight to pixels. The 13-skill systems-diagnostic suite (`problem-triage` → `system-sensing` → `edge-diagnostics` → `root-cause-hypothesis-testing` → `evidence-planning` → `intervention-sizing` → `adoption-and-ownership-planning` → `learning-loop-design` → `executive-diagnostic-synthesis`, orchestrated by `system-aware-diagnostic-kernel` / `system-diagnostic-command-reference`) follows the same pattern. Resist the urge to fold a new capability into an existing skill if it's really a new stage — give it its own folder and wire the handoff via descriptions instead.

**4. Every governed-content skill (writing, data governance, AI governance) asks for the same metadata skeleton**: owner, steward, evidence, review cadence, approval, exceptions with expiration. Keep new skills in these families consistent with that skeleton rather than inventing a different one.

**5. `commands/` are orchestrators, not authors.** A command file lists required inputs, then chains skills in numbered phases (see `commands/build-governance-bundle.md`: 6 phases invoking ~20 skills by name, closing with an 18-section default output structure) or points to `skills/build-governance-bundle` which does the equivalent inline. When adding a command, follow this shape — collect inputs, phase-order the skill applications by name, define the output section list — rather than writing new domain guidance directly into the command file.

## Skill file structure

Each skill folder contains `SKILL.md` with YAML frontmatter (`name`, `description`, optionally `argument-hint`) followed by Markdown body sections that vary by skill but commonly include: `## When to Use`, an ordered `## Orchestration Order` or `## Steps`, `## Required Inputs`, `## Output Template` (literal Markdown skeleton), and `## Quality Checklist`. Some skills add `references/` or `templates/` subfolders (mirroring the pattern used by `finance-documentation-lifecycle`, which has richer content in its live `.cursor/skills/` copy than the snapshot here — see that skill's own `CLAUDE.md` for the caveat about which copy is current).

The **`description` field is the routing mechanism** — it's what an agent harness matches against user intent, so it must state both what the skill does and when to use it (often with explicit "use when..." / "use X instead when..." language). Keep it a single dense paragraph; don't rely on the body for disambiguation the description should carry.

## Agents — orchestrating skills as a team, not one long context

`agents/` holds subagents in the format `cursor-workflow-skills/create-subagent/SKILL.md` documents (frontmatter `name` + `description`, body = system prompt, installed to `.cursor/agents/`). This exists because commands like `build-governance-bundle` chain 12–20 skills through a single context applying them one at a time — no parallelism between independent phases, and nothing checks the assembled result before it ships.

The pilot (`governance-bundle-orchestrator` + `data-governance-foundation-agent` + `data-quality-agent` + `governance-writing-agent` + `governance-bundle-qa-agent`) covers `build-governance-bundle` only. Its shape, to reuse when piloting another command:

- **One orchestrator per command family**, not per command — it reads the command/skill file for the phase plan rather than duplicating it, collects required inputs (and asks rather than guesses when one is missing), delegates phases to named specialists, runs independent phases concurrently, assembles into the skill's own output template, and gates through QA before returning to the user.
- **Specialist agents are clustered by theme, not one-per-skill** — `data-governance-foundation-agent` alone carries 4 skills. Each specialist's roster is written as a subset of a larger intended cluster (documented in the agent file itself); extend an existing specialist's roster before creating a new agent when a new command needs a skill from a theme already covered.
- **A QA/verification agent is the one genuinely new capability**, not a reorganization of an existing skill — it adversarially checks the assembled bundle against the skill's own "Quality Checklist" section plus cross-artifact consistency (glossary vs. every other artifact's terminology, metric definitions vs. every reference to them), and only reports findings; it never fixes content itself, and findings route back to the owning specialist, not to the orchestrator.

When piloting a second command (e.g. `build-analytics-governance-bundle` or `build-finance-ai-governance-bundle`), reuse `data-governance-foundation-agent` / `governance-writing-agent` / `governance-bundle-qa-agent` and extend their rosters rather than forking new agents, and only add a genuinely new specialist for a theme not yet covered (e.g. a `finance-ai-governance-agent` for `internal-control-design` + the `finance-ai-*` skills, or a `dashboard-product-agent` for the dashboard skill family).

## Finance domain layer

Most of the library is domain-agnostic (data governance, data quality, dimensional modeling, the diagnostic suite). A thinner set of skills adds finance/accounting specificity on top — `finance-ai-use-case-intake` → `finance-ai-risk-control-mapping` → `finance-ai-safe-use-policy` → `ai-agent-readiness-assessment` (intake and risk tiering always precede policy and deployment approval), plus `finance-dashboard-design`, `finance-documentation-lifecycle`, `financial-variance-analysis`, `reconciliation-analytics`. These mostly add compliance vocabulary (SOX, audit evidence) rather than a different underlying method — keep new finance-specific skills thin wrappers over the general pattern rather than duplicating it.

## Relationship to other repos on this machine

This skill library is very likely the working set used to produce `C:\Users\brian\control-governance\` — `build-governance-bundle`'s orchestration order and 13-item output template match that repo's `01-controlled-operations.md` / `02-governed-data-and-analytics.md` / `03-governed-ai.md` package-bundle pattern almost exactly. If asked to extend either repo, check the other for an existing pattern to reuse before inventing a new one.

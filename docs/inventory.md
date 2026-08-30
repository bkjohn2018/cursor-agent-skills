# Skills And Commands Inventory

This inventory lists the skill folders and command files included in the repository.

## Primary Domain Skills

### AI And Finance Controls

- `ai-agent-readiness-assessment`
- `finance-ai-risk-control-mapping`
- `finance-ai-safe-use-policy`
- `finance-ai-use-case-intake`
- `internal-control-design`

### Analytics And Finance

- `analytics-storytelling`
- `descriptive-pattern-analysis`
- `finance-dashboard-design`
- `financial-variance-analysis`
- `predictive-model-development`
- `question-driven-data-projects`
- `reconciliation-analytics`

### Dashboard And Webspace

- `dashboard-frontend-implementation`
- `dashboard-information-architecture`
- `dashboard-metric-semantics`
- `dashboard-product-framing`
- `governance-dashboard-content-model`
- `pbip-build-verification`

### Data Governance And Management

- `business-glossary-management`
- `data-capability-roadmapping`
- `data-coe-operating-model`
- `data-governance`
- `data-governance-mvdg-launch`
- `data-issue-management`
- `data-management-foundations`
- `data-management-maturity-assessment`
- `data-security-and-privacy-controls`
- `data-standards-management`
- `data-strategy-lifecycle`
- `data-strategy-scorecard`
- `metadata-and-lineage`

### Data Quality And Modeling

- `data-model-requirements-and-quality`
- `data-model-scorecard-review`
- `data-profiling`
- `data-quality-assessment`
- `data-quality-controls`
- `dimensional-modeling`

### Discovery Workspace

- `discovery-analyst`
- `discovery-workspace`

### Documentation, Policy, And Communication

- `architecture-ppt-deck-writing`
- `build-governance-bundle`
- `executive-summary-writing`
- `finance-documentation-lifecycle`
- `governance-ppt-deck-writing`
- `governance-project-delivery`
- `governance-writing-style-guide`
- `metric-governance`
- `policy-and-standard-writing`
- `process-and-procedure-writing`
- `sop-writing`

### System Diagnostics

- `adoption-and-ownership-planning`
- `diagnostic-scope-control`
- `edge-diagnostics`
- `evidence-planning`
- `executive-diagnostic-synthesis`
- `facilitation-design`
- `intervention-sizing`
- `learning-loop-design`
- `people-process-technology-diagnostics`
- `problem-triage`
- `root-cause-hypothesis-testing`
- `system-aware-diagnostic-kernel`
- `system-diagnostic-command-reference`
- `system-sensing`
- `systems-failure-mode-check`

## Agents (Pilot)

Subagents in `agents/`, orchestrating the skills above as a delegated team rather than one context
applying every chained skill. Currently scoped to `build-governance-bundle` only.

- `governance-bundle-orchestrator` — collects inputs, delegates phases, assembles, gates
- `data-governance-foundation-agent` — `question-driven-data-projects`, `data-management-foundations`, `data-governance`, `metadata-and-lineage`
- `data-quality-agent` — `data-quality-controls`, `data-quality-assessment` (renamed from `data-quality-controls-agent` 2026-08-02 when scope expanded)
- `governance-writing-agent` — `business-glossary-management`, `metric-governance`, `governance-writing-style-guide`, `process-and-procedure-writing`, `sop-writing`, `executive-summary-writing`, `governance-ppt-deck-writing`
- `governance-bundle-qa-agent` — adversarial check against the bundle's own quality checklist; new capability, not a wrapper around an existing skill

Each specialist's roster is written as the seed of a larger cluster (see `agents/governance-bundle-orchestrator.md`'s closing note) — extend rosters in place before creating new agents when piloting additional commands.

## Cursor Workflow Skills

- `babysit`
- `canvas`
- `create-hook`
- `create-rule`
- `create-skill`
- `create-subagent`
- `migrate-to-skills`
- `sdk`
- `shell`
- `split-to-prs`
- `statusline`
- `update-cli-config`
- `update-cursor-settings`

## Cursor Commands

### Governance Bundles

- `adapt-governance-guide.md`
- `build-analytics-governance-bundle.md`
- `build-finance-ai-governance-bundle.md`
- `build-governance-bundle.md`
- `create-governance-package.md`
- `refresh-governance-package.md`
- `review-governance-package.md`

### Dashboard And Webspace

- `build-dashboard-shell.md`
- `define-dashboard-metrics.md`
- `design-dashboard-page.md`
- `plan-dashboard-webspace.md`
- `review-dashboard-semantic-consistency.md`
- `review-dashboard-ux.md`

## Legacy Agent Skills

These are preserved from the older `.agents\skills` location.

- `data-quality-controls`
- `executive-summary-writing`
- `governance-writing-style-guide`
- `metric-governance`
- `sop-writing`

## Sync Source

The active runtime copies live in:

- `C:\Users\brian\.cursor\skills`
- `C:\Users\brian\.cursor\commands`

This repository is the portable distribution package for GitHub and ZIP install.

Local clone path:

- `C:\Users\brian\cursor-agent-skills`

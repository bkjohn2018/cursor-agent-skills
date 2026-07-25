# Session Handoff

**Last updated:** 2026-07-11

This is a living handoff doc — update it in place at the end of a work session rather than creating a new dated file, same convention as `sync-status.md`.

## What this session did

1. Wrote `CLAUDE.md` files for the real projects living under the messy home-directory git repo: `fixed-assets-subledger/`, `control-governance/` (plus scoped ones for `control-governance/design/` and `control-governance/architecture/`), `.cursor/skills/finance-documentation-lifecycle/`, `cursor-agent-skills/`, and `projects/dama-exam-study-guide/`.
2. Reviewed the `cursor-agent-skills` library end to end and identified 6 cross-cutting design themes (staged-pipeline skill handoffs, framework-anchoring, deliberate narrow decomposition, shared governance metadata skeleton, native/process-before-AI discipline, self-extending meta-tooling).
3. Designed a multi-agent team to orchestrate skills/commands (orchestrator → 6 thematic specialists → QA gate), then **piloted it scoped to `build-governance-bundle` only**: 1 orchestrator + 3 specialists + 1 QA gate, in `cursor-agent-skills/agents/`.
4. Dry-run tested the pilot twice via Claude Code's Agent tool (test domain: **Treasury Cash Positioning**, chosen because it's new and doesn't collide with `control-governance`'s existing 8 domains). Round 1 found 5 real issues (RACI/control conflation, a metric with no exact-match glossary entry, role-name drift across phases, 3 silently-uncovered output-template sections, no Bundle Inputs recap). All 5 fixed. Round 2 re-test confirmed the fixes held **and** the QA gate — working blind, not told what to look for — caught 2 more real issues on its own (a stale hardcoded gap list, the same undefined-glossary-term bug recurring from a different specialist). Both fixed. Pilot considered validated after round 2.
5. Synced `agents/` to `.cursor/agents/` (created fresh — didn't exist before this session). Full test history is logged in `cursor-agent-skills/docs/sync-status.md`.
6. Raised and investigated: **is this content prepared for the Oracle Fusion 26B → 26C release bump?** Answer: no. See open thread below.
7. Looked up actual Oracle 26C release notes (`docs.oracle.com` only, per standing preference — see `feedback_oracle-sourced-docs-only` memory). Confirmed release timing and pulled verified Fixed Assets and Payables feature details. See "Oracle 26C release notes findings" below.

## Where things stand right now

- `cursor-agent-skills/agents/` and `.cursor/agents/` are in sync (verified byte-identical). 5 files: `governance-bundle-orchestrator.md`, `data-governance-foundation-agent.md`, `data-quality-controls-agent.md`, `governance-writing-agent.md`, `governance-bundle-qa-agent.md`.
- The pilot has **only been dry-run tested via Claude Code's Agent tool**, standing in for Cursor's native subagent delegation. It has **not yet been tried live inside Cursor itself** — that's the natural next validation step before trusting it for real bundle builds.
- Pilot scope is deliberately narrow: only the 12 skills `build-governance-bundle` chains. See "Extension backlog" below for what's not covered yet.

## Open thread: Oracle 26B → 26C readiness

Investigated but not acted on. Findings:

- **`fixed-assets-subledger`**: 24 files reference `26B` (including a `version: 26B` field in every `contracts/*/*.yml`). A manual update process *is* documented (`docs/platform/change-discipline.md`: contracts → SQL → Power BI → re-validate), but `scripts/validate_contracts.py` only checks that a `version` key exists, never that its *value* is consistent across contracts or matches a canonical current release — a partial/inconsistent update would pass CI silently.
- **`control-governance`**: 31 files reference `26B`, and it's structurally worse — the release number is baked into **8 package directory names** (`packages/oracle-fusion-fixed-assets-26b/`, etc.), cross-linked from the root README, `CLAUDE.md`, the CapEx overlay, the MDM framework, and the dashboard IA spec's Domain Reference table. **No migration policy is written down anywhere** for whether a version bump means renaming those 8 directories in place (breaks every internal link, loses the old snapshot) or standing up parallel `-26c` packages (doubles maintenance, needs real re-validation against 26C behavior, not just a relabel).
- **The agent pilot itself has zero `26B` coupling** — verified via grep, `agents/` is release-agnostic by design and needs no change for this.
- Timing note (corrected after research below): Oracle 26C production go-live is **2026-08-21** for the first customer cohort (Cohort B mid-September, Cohort C mid-October) — not live yet as of this session, but close.

**Next steps identified:**
1. Strengthen `validate_contracts.py` to check every contract's `version` value against one canonical source (e.g. a single `RELEASE` marker file or the README), not just presence. **Not started.**
2. Write the actual `control-governance` migration policy (rename-in-place vs. archive-and-parallel) — this decision should be made deliberately, not improvised under time pressure at the next bump. **Not started.**
3. ~~Look up Oracle's actual 26C release notes~~ **Done — see findings below.** Still needed: GL, Cash Management, and Project Financial Management weren't covered by this pass; only Assets and Payables were confirmed.
4. **New, higher-priority than #1/#2**: run the 3 confirmed 26C AI agent features (Fixed Asset Inquiry Assistant, Retirement Assistant, Payables Agent for Invoice Ingestion/Compliance/Control) through `finance-ai-use-case-intake` → `finance-ai-risk-control-mapping` → `finance-ai-safe-use-policy` before any security-role enablement, and check whether `oracle-fusion-fixed-assets-26b/03-governed-ai.md` and `oracle-fusion-ap-i2p-26b/03-governed-ai.md` need updating to address them by name. This is a governance-content gap, not a version-string housekeeping gap — see finding below for why it matters more.

## Oracle 26C release notes findings (2026-07-11, `docs.oracle.com` only)

Researched per the standing "Oracle-sourced docs only" preference (see `feedback_oracle-sourced-docs-only` memory) — third-party "release intelligence" aggregators were tried first and rejected as unreliable (suspiciously specific, unverifiable content from unofficial sources).

**Confirmed via official Oracle readiness docs:**

- **Fixed Assets** — 3 new features, all enabled by default, all conversational AI agents requiring explicit security-console role setup before use:
  - *Fixed Asset Inquiry Assistant* — natural-language asset/activity lookup. Limits: English only, single book per query, max 10 recent assets, max 5 recent transactions.
  - *Retirement Assistant* — guided conversational retirement processing, batch up to 10 assets, exception handling.
  - *Retirement Request Assistant* — requester-side counterpart (found in feature index, not individually fetched).
- **Payables** — 2 new features:
  - *Payables Agent for Invoice Ingestion, Compliance and Control* — AI agent covering intake, policy-driven completion, anomaly detection, conversational invoice-list UI. Enabled by default; needs multiple duty-role/privilege and Business Unit data-security configurations.
  - *Invoice Import with Supplier Bank Account Details via Collaboration Messaging Framework* — B2B XML invoices now carry remit-to bank/IBAN through to installments automatically. Enabled by default, no config needed. Touches `AP_INVOICES_INTERFACE` (`EXTERNAL_BANK_ACCOUNT_NUMBER`, `EXT_BANK_ACCOUNT_IBAN_NUMBER`).
- **Not verified this pass**: General Ledger, Cash Management, Project Financial Management. Absence of findings there means "wasn't confirmed," not "confirmed unchanged." No deprecated/removed features were mentioned in anything fetched, but that wasn't checked exhaustively either.

**The finding that matters most**: every confirmed Financials-relevant 26C feature is an AI agent, not an ordinary functional change. That makes this a `control-governance` AI-governance question (route through the existing `03-governed-ai.md` / finance-AI-intake skill chain) before it's a `fixed-assets-subledger` contracts/SQL question — a more consequential 26C-readiness item than the version-string housekeeping in next-steps #1/#2 above.

**Sources** (all `docs.oracle.com`):
- [Financials 26C What's New — Revision History](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-t74312.htm)
- [Fixed Asset Inquiry Assistant](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f49378.htm)
- [Retirement Assistant](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f49559.htm)
- [Payables Agent for Invoice Ingestion, Compliance and Control](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f49574.htm)
- [Invoice Import with Supplier Bank Account Details Using Collaboration Messaging Framework](https://docs.oracle.com/en/cloud/saas/readiness/erp/26c/fins26c/26C-fin-wn-f49280.htm)

## Extension backlog for the agent pilot (recommended, not built)

From the original team recommendation, only 3 of 6 proposed specialist clusters exist (as pilot-scoped subsets, not their full proposed rosters):

| Specialist | Status |
|---|---|
| `data-governance-foundation-agent` | Built, pilot-scoped (4 of ~10 proposed skills) |
| `data-quality-controls-agent` | Built, pilot-scoped (1 of ~6 proposed skills) |
| `governance-writing-agent` | Built, pilot-scoped (7 of ~10 proposed skills) |
| `governance-bundle-qa-agent` | Built, new capability (no prior equivalent existed) |
| `diagnostics-agent` (13-skill systems-diagnostic suite) | Not built |
| `finance-ai-governance-agent` (`internal-control-design` + `finance-ai-*` cluster) | Not built |
| `dashboard-product-agent` (dashboard/analytics family) | Not built |

Guidance already encoded in the agent files: extend an existing specialist's roster in place before creating a new agent, unless a new command needs a genuinely uncovered theme.

## Files touched this session (for orientation on resume)

- `fixed-assets-subledger/CLAUDE.md`
- `control-governance/CLAUDE.md`, `control-governance/design/CLAUDE.md`, `control-governance/architecture/CLAUDE.md`
- `.cursor/skills/finance-documentation-lifecycle/CLAUDE.md`
- `cursor-agent-skills/CLAUDE.md`, `README.md` (layout updated), `docs/inventory.md` (Agents section added), `docs/sync-status.md` (agents tracked, full test log), `docs/handoff.md` (this file)
- `cursor-agent-skills/agents/*.md` (5 files) and `.cursor/agents/*.md` (synced copies)
- `projects/dama-exam-study-guide/CLAUDE.md`
- `~/.claude/projects/C--Users-brian/memory/feedback_oracle-sourced-docs-only.md` (+ `MEMORY.md` index) — standing preference, not project-specific

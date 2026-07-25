# Sync Status

Last synced from active Cursor locations on 2026-07-02.

See `docs/handoff.md` for the current open work items and where the last session left off — check it first when resuming.

## Repository Location

- Local clone: `C:\Users\brian\cursor-agent-skills`
- GitHub: `https://github.com/bkjohn2018/cursor-agent-skills`

## Source Of Truth (Runtime)

- Skills: `C:\Users\brian\.cursor\skills`
- Commands: `C:\Users\brian\.cursor\commands`
- Workflow skills: `C:\Users\brian\.cursor\skills-cursor`
- Agents: `C:\Users\brian\.cursor\agents` (created 2026-07-11 to run the `build-governance-bundle` pilot; now the runtime source, same as skills/commands above)

## Distribution Package (This Repo)

- Skills: `skills/`
- Commands: `commands/`
- Workflow skills: `cursor-workflow-skills/`
- Agents: `agents/`

## Current Counts

| Area | Count |
|---|---:|
| Domain skills | 62 |
| Commands | 13 |
| Workflow skills | 13 |
| Agents | 5 (1 orchestrator + 3 specialists + 1 QA gate; pilot scope, `build-governance-bundle` only) |

## Sync Procedure

1. Copy all folders from `.cursor\skills` to `skills\` with overwrite.
2. Copy all `*.md` from `.cursor\commands` to `commands\` with overwrite.
3. Update `docs\inventory.md` if new packs were added.
4. Commit and push from `cursor-agent-skills`.

Note: `agents/` currently syncs in the opposite direction from the procedure above — it is authored in this
repo first, then copied to `.cursor\agents` (last done 2026-07-11, after dry-run testing and fixes). Revisit
this once agents are edited directly at runtime rather than in the distribution repo.

## Notes

- Keep this repository at `C:\Users\brian\cursor-agent-skills` for visibility and easy access.
- Workflow skills in `cursor-workflow-skills/` should be compared separately against `.cursor\skills-cursor` when Cursor tooling skills change.
- `agents/` pilot (`build-governance-bundle` only) was dry-run tested via Claude Code's Agent tool on
  2026-07-11 (test domain: Treasury Cash Positioning) across two full rounds before being copied to
  `.cursor\agents`:
  - Round 1 found: RACI/GL-cash-tie-out conflation with the unowned daily reconciliation control; a
    metric-glossary self-check gap (a metric named with no exact-match glossary entry); role-name drift
    between phases (`Analyst`/`Cash Mgmt Analyst`/`Treasury Analyst` used for one role, an invented
    "Controller delegate"); 3 Output Template sections silently unproduced; no Bundle Inputs recap.
  - Fixes applied: orchestrator writes Bundle Inputs itself and checks template-section coverage against
    the live specialist roster; writing agent's self-check requires an exact-name glossary match, not a
    looser "traces to" relationship; foundation agent now produces a canonical roles list plus explicit
    disambiguation of confusable controls, which every later phase must reuse verbatim.
  - Round 2 re-test confirmed all of round 1's findings fixed, and the QA gate (working independently, not
    told what to look for) found two new/residual issues on its own: the hardcoded 3-section gap list was
    already stale (RACI and Issue Management also have no owning specialist), and a DQ rule introduced an
    undefined glossary term the same way the round-1 metric had. Both fixed: the orchestrator's section
    check is now general (derive coverage from the live roster, not a fixed list) rather than a hardcoded
    list, and `data-quality-controls-agent` now runs the same glossary cross-check discipline the writing
    agent has.
  - Pilot considered validated after round 2 — the QA gate demonstrated it catches real, non-repeated
    issues across two independent runs rather than rubber-stamping. Not re-tested a third time; further
    validation should happen through real use.

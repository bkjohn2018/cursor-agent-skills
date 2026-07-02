# Sync Status

Last synced from active Cursor locations on 2026-07-02.

## Repository Location

- Local clone: `C:\Users\brian\cursor-agent-skills`
- GitHub: `https://github.com/bkjohn2018/cursor-agent-skills`

## Source Of Truth (Runtime)

- Skills: `C:\Users\brian\.cursor\skills`
- Commands: `C:\Users\brian\.cursor\commands`
- Workflow skills: `C:\Users\brian\.cursor\skills-cursor`

## Distribution Package (This Repo)

- Skills: `skills/`
- Commands: `commands/`
- Workflow skills: `cursor-workflow-skills/`

## Current Counts

| Area | Count |
|---|---:|
| Domain skills | 62 |
| Commands | 13 |
| Workflow skills | 13 |

## Sync Procedure

1. Copy all folders from `.cursor\skills` to `skills\` with overwrite.
2. Copy all `*.md` from `.cursor\commands` to `commands\` with overwrite.
3. Update `docs\inventory.md` if new packs were added.
4. Commit and push from `cursor-agent-skills`.

## Notes

- Keep this repository at `C:\Users\brian\cursor-agent-skills` for visibility and easy access.
- Workflow skills in `cursor-workflow-skills/` should be compared separately against `.cursor\skills-cursor` when Cursor tooling skills change.

# Cursor Agent Skills And Commands

This repository packages reusable Cursor and agent skills, plus custom Cursor commands, as plain Markdown-first files. It is intended for simple GitHub browsing and ZIP download, especially when moving skills and commands to another machine.

Each skill lives in its own folder and uses `SKILL.md` as the entry point. Some skills also include supporting templates, references, or SDK type files.

## Repository Layout

```text
skills/
  Domain skills for finance, data, governance, analytics, documentation, and AI controls.

cursor-workflow-skills/
  Cursor workflow skills for creating skills, rules, hooks, canvases, SDK usage, PR workflows, and related tooling.

commands/
  Custom Cursor command Markdown files.

legacy-agent-skills/
  Older `.agents` copies retained for reference where they overlap with primary skills.

docs/
  Installation and inventory documentation.
```

## Download And Install

The simplest workflow is:

1. Open the GitHub repository.
2. Select **Code** > **Download ZIP**.
3. Extract the ZIP on the target machine.
4. Copy selected folders from `skills/` into the target Cursor skills folder.
5. Copy selected folders from `cursor-workflow-skills/` only if those workflow skills are needed.
6. Copy selected files from `commands/` into the target Cursor commands folder.
7. Restart Cursor and verify the skills and commands are available.

See `docs/install-from-zip.md` for detailed Windows-oriented instructions.

## Notes

- Treat `skills/` as the primary source for the current domain skills.
- Treat `commands/` as the primary source for custom command Markdown files.
- Treat `legacy-agent-skills/` as historical reference unless you intentionally need an older copy.
- Keep each skill self-contained so individual folders can be downloaded or copied without a build step.


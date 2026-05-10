# Install From GitHub ZIP

Use this process when the target machine can access the public GitHub repository but does not need Git installed or configured.

## Download

1. Open the repository on GitHub.
2. Select **Code**.
3. Select **Download ZIP**.
4. Extract the ZIP to a temporary folder, such as `Downloads\cursor-agent-skills`.

## Install Domain Skills

Copy the skill folders you want from:

```text
skills\
```

to the Cursor user skills folder on the target machine:

```text
%USERPROFILE%\.cursor\skills\
```

Example target path:

```text
C:\Users\<your-user>\.cursor\skills\data-governance\SKILL.md
```

## Install Cursor Workflow Skills

Copy workflow skill folders only when needed from:

```text
cursor-workflow-skills\
```

to the target machine's Cursor workflow skill location if you use a separate folder, or into the same user skills folder if that is how the machine is configured.

Common target:

```text
%USERPROFILE%\.cursor\skills-cursor\
```

## Install Commands

Copy the command Markdown files you want from:

```text
commands\
```

to the Cursor user commands folder on the target machine:

```text
%USERPROFILE%\.cursor\commands\
```

Example target path:

```text
C:\Users\<your-user>\.cursor\commands\create-governance-package.md
```

## Legacy Skills

The `legacy-agent-skills\` folder preserves older `.agents` versions for reference. Do not install these over the primary `skills\` versions unless you specifically need the older content.

## Verify

After copying the folders:

1. Restart Cursor.
2. Start a new chat.
3. Ask for a task that should trigger one of the installed skills.
4. Use the command menu to confirm the installed commands are available.
5. Confirm the skill appears in the available skills list or is used by the agent.

If a skill is not recognized, confirm that the folder contains `SKILL.md` directly inside the skill folder.
If a command is not recognized, confirm that the `.md` command file is directly inside the commands folder.


# Install Guide

This is a practical installation checklist for adapting the template to a new machine.

## 1. Choose Local Paths

Recommended layout:

```text
~/Documents/04 Codex/
  _Global Codex Memory/
  <project-name>/
```

You can use any path. Just make sure the path in `~/.codex/AGENTS.md` matches the real memory folder.

## 2. Install Global Rules

Copy:

```text
global/AGENTS.md
```

to:

```text
~/.codex/AGENTS.md
```

Then replace:

```text
{{CODEX_GLOBAL_MEMORY_DIR}}
```

with your actual global memory path.

## 3. Install Global Memory

Copy:

```text
global/memory/
```

to your chosen long-term folder, for example:

```text
~/Documents/04 Codex/_Global Codex Memory/
```

## 4. Start A New Project

For each long-term project:

1. Create a project folder.
2. Copy `project-template/AGENTS.md` into that project root.
3. Create `docs/codex/`.
4. Generate project memory files from the templates in `global/memory/templates/`.

## 5. Recommended First Prompt

After installing, open Codex in a project folder and say:

```text
Please read this project's AGENTS.md and initialize the project memory structure. Before writing any files, explain what you plan to create and wait for my confirmation.
```

## 6. Maintenance

Update memory carefully:

- Write project facts into project memory.
- Write cross-project lessons into global memory only after they repeat or become stable.
- Do not write secrets, credentials, private chats, or raw personal data into memory.
- When in doubt, ask Codex to propose a memory update first, then review it before saving.

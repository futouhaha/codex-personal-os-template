# Codex Personal OS Template

This repository is a shareable template for building a personal Codex collaboration system.

It contains:

- a global `AGENTS.md` entry file
- a global memory folder for reusable collaboration rules and protocols
- project-level `AGENTS.md` and memory templates
- prompts and policies for task routing, onboarding, retrospectives, browser safety, tooling, and skills

The template is intentionally written with placeholders. Replace them before using it.

## Folder Structure

```text
global/
  AGENTS.md
  memory/
    00_INDEX.md
    01_WORKING_STYLE.md
    02_TASK_ROUTING.md
    03_PROJECT_ONBOARDING_PROTOCOL.md
    04_MEMORY_AND_RETROSPECTIVE_POLICY.md
    05_BROWSER_AND_SECURITY_POLICY.md
    06_TOOLING_AND_INSTALL_POLICY.md
    07_SKILL_STRATEGY.md
    08_CROSS_PROJECT_LEARNINGS.md
    09_REUSABLE_PROMPTS.md
    templates/
project-template/
  AGENTS.md
  docs/codex/
```

## Placeholders

Before installing, replace these placeholders:

- `{{USER_NAME}}`: your name or preferred nickname
- `{{user_name}}`: lowercase username if needed
- `{{CODEX_PROJECTS_ROOT}}`: where you keep long-term Codex projects
- `{{CODEX_GLOBAL_MEMORY_DIR}}`: where you keep the copied global memory folder

Example:

```text
{{CODEX_PROJECTS_ROOT}} = /Users/yourname/Documents/04 Codex
{{CODEX_GLOBAL_MEMORY_DIR}} = /Users/yourname/Documents/04 Codex/_Global Codex Memory
```

## Suggested Installation

1. Copy `global/AGENTS.md` to your Codex global agent file, usually:

```text
~/.codex/AGENTS.md
```

2. Copy `global/memory/` to your preferred long-term memory location.

3. Edit `~/.codex/AGENTS.md` so its memory path points to your actual `global/memory/` folder.

4. For a long-term project, copy `project-template/AGENTS.md` into the project root and create a project memory folder such as:

```text
docs/codex/
```

5. Use the templates in `global/memory/templates/` to create project-specific memory files.

## Important Safety Notes

Do not commit or share:

- `~/.codex/auth.json`
- local logs or SQLite state files
- API keys, tokens, passwords, `.env` files, or account screenshots
- raw personal memory that has not been reviewed

This repository is a system template, not a dump of someone else's private Codex configuration.

## How To Use With A Friend

Send them the repository link and tell them:

1. Read this README first.
2. Replace placeholders with their own paths and name.
3. Start with the global `AGENTS.md` and `00_INDEX.md`.
4. Do not blindly copy project memories from another person.
5. Create their own project memories only after a real project has stable needs.

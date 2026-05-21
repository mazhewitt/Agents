# GitHub Copilot Agents and Skills

This folder contains GitHub Copilot–native variants of the shared agent and skill set.

## What belongs here

- **`agents/`** — Copilot agent definitions. These are instruction files for GitHub Copilot's coding agent (or task agent), invoked via the GitHub Copilot interface or `.github/agents/` conventions.
- **`skills/`** — Reusable instruction modules that can be referenced in agent prompts or used directly in a Copilot session.

## Design principles

- All content here is **repository-independent**. No references to specific project names, codebases, infrastructure, or environments.
- Use "the project's domain glossary", "the repository's architecture docs", "any ADRs or design notes in the area", and similar generic phrasing rather than hardcoded paths.
- Copilot-specific formatting: frontmatter contains only `description` (no `model` or `tools` fields, which are Claude-specific). Instructions are framed for Copilot's GitHub-integrated operation style.

## Agents

| Agent | Purpose |
|---|---|
| `critic.md` | Adversarial reviewer — pressure-tests work before it's accepted |
| `doc-updater.md` | Conservative documentation maintainer |
| `implementor.md` | Focused TDD implementor for mechanical tasks |

## Skills

| Skill | Purpose |
|---|---|
| `diagnose/` | Disciplined debug loop: reproduce → hypothesise → instrument → fix |
| `handoff/` | Compact a conversation into a handoff doc for the next session |
| `improve-codebase-architecture/` | Find and propose deepening opportunities in a codebase |
| `prototype/` | Build throwaway prototypes to answer design questions |
| `tdd/` | Red-green-refactor loop with companion docs |
| `zoom-out/` | Ask for a higher-level map of a code area |

## See also

- [`../claude/`](../claude/README.md) — Claude variants of the same agents and skills

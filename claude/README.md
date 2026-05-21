# Claude Agents and Skills

This folder contains Claude-native variants of the shared agent and skill set.

## What belongs here

- **`agents/`** — Claude sub-agent definitions (YAML frontmatter + instruction body). These are invoked by a parent Claude session using the `claude --agent` mechanism or equivalent.
- **`skills/`** — Reusable instruction modules that agents and the main session can invoke via the `Skill` tool.

## Design principles

- All content here is **repository-independent**. No references to specific project names, codebases, infrastructure, or environments.
- Use "the project's domain glossary", "the repository's architecture docs", "any ADRs or design notes in the area", and similar generic phrasing rather than hardcoded paths.
- Claude-specific formatting is preserved: YAML frontmatter includes `tools` and `model` fields understood by Claude's agent runtime.

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

- [`../copilot/`](../copilot/README.md) — GitHub Copilot variants of the same agents and skills

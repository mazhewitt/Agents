# Agents

A collection of reusable agents and skills for AI-assisted software development.

## Structure

```
agents/          Original agent definitions (preserved)
skills/          Original skill definitions (preserved)

claude/          Claude-native variants
  agents/
  skills/
  README.md

copilot/         GitHub Copilot–native variants
  agents/
  skills/
  README.md
```

## Two platform variants

The `claude/` and `copilot/` trees contain the same logical set of agents and skills, rewritten for each platform:

- **`claude/`** — Uses Claude's native agent format: YAML frontmatter with `tools` and `model` fields, Claude tool names, and Claude-style skill invocation.
- **`copilot/`** — Uses GitHub Copilot's agent format: simplified `description`-only frontmatter, framed for Copilot's GitHub-integrated operation style.

Both variants are **repository-independent**: all project-specific references have been removed and replaced with generic language (e.g. "the project's domain glossary", "any ADRs or design notes in the area"). They can be dropped into any repository.

## Agents

| Agent | Purpose |
|---|---|
| `critic` | Adversarial reviewer — pressure-tests work before it's accepted |
| `doc-updater` | Conservative documentation maintainer |
| `implementor` | Focused TDD implementor for mechanical, well-scoped tasks |

## Skills

| Skill | Purpose |
|---|---|
| `diagnose` | Disciplined debug loop: reproduce → hypothesise → instrument → fix |
| `handoff` | Compact a conversation into a handoff doc for the next session |
| `improve-codebase-architecture` | Find and propose deepening opportunities in a codebase |
| `prototype` | Build throwaway prototypes to answer design questions |
| `tdd` | Red-green-refactor loop with companion docs |
| `zoom-out` | Ask for a higher-level map of a code area |

## Original source material

The `agents/` and `skills/` folders contain the original versions, preserved for reference.

# [Your Team Name] Claude Agents

This project uses Claude Code's multi-agent system to automate [describe what your pipeline does].

---

## Agents

Agents live in `.claude/agents/`. Each agent is a markdown file with a YAML frontmatter header.

| Agent | Model | Role |
|---|---|---|
| `example-agent` | sonnet | Describe what this agent does |

Add or remove rows as you define your own agents. See `.claude/agents/example-agent.md` for the template.

---

## Skills (Slash Commands)

Skills live in `.claude/skills/`. Each skill is a folder with a `SKILL.md` file inside.

| Command | What it triggers |
|---|---|
| `/example-skill` | Describe the pipeline this kicks off |

Type the command in Claude Code to start the pipeline.

---

## Pipeline Order

Define the order your agents run. Example:

```
User input
    ↓
@researcher
    ↓
@writer
    ↓
@reviewer
    ↓
⏸ Pause — human reviews
    ↓
@formatter
    ↓
Output file saved to ./outputs/
```

---

## Rules

- All output files must be saved to `./outputs/` — never write to the repo root
- [Add your own rules here]

---

## Versioning

This repo uses [CHANGELOG.md](CHANGELOG.md) (Keep a Changelog format) and Semantic
Versioning (`MAJOR.MINOR.PATCH`).

**What counts as a functional change** (requires a version bump — this is a
template repo, so "functional" means it changes what happens when someone
clones and runs it):

- `.claude/agents/*.md` — adding, removing, or changing an agent's behavior, model, or tools
- `.claude/skills/**/SKILL.md` — adding, removing, or changing a slash command's pipeline
- `.claude/settings.json` — permission or hook changes
- Root `CLAUDE.md` — changes to the pipeline order or rules (the sections above this one)

**Not a functional change** (no bump needed): README prose/formatting, `.gitignore`,
comments, typo fixes in docs, or anything else that doesn't change what an
agent/skill actually does when run.

**Version bump rules:**
- **MAJOR** — breaking or workflow-changing (e.g. renamed/removed agent or skill, changed pipeline order)
- **MINOR** — new capability (new agent, new skill, new tool granted)
- **PATCH** — fix or tweak to existing agent/skill behavior

**On every commit with a functional change**, proactively (without being asked):
1. Add an entry under `## [Unreleased]` in [CHANGELOG.md](CHANGELOG.md) (Added/Changed/Fixed/Removed), then move it under a new version heading dated with the commit date.
2. Bump the version in `CHANGELOG.md` and in the `**Version:**` line in `README.md` — keep both in sync.

---

## Context

- [Describe your team, product, or domain here so agents have grounding]
- [Add any terminology, personas, or constraints that agents should know]

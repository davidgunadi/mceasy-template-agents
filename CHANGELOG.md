# Changelog

All notable changes to this repo are documented in this file.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and versioning follows [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.1.0] - 2026-07-07

### Added

- `./scripts/` folder convention: any script invoked by an agent while running must live there, not in the repo root. Referenced in `CLAUDE.md` rules and `README.md`'s folder structure.

## [1.0.0] - 2026-07-06

### Added

- Initial multi-agent template scaffold: `.claude/agents/example-agent.md` and `.claude/skills/example-skill/` as starting points for custom agents and slash commands.
- `.claude/settings.json` for tool permissions.
- Root `CLAUDE.md` defining the agent/skill/pipeline structure and repo rules (e.g. outputs go to `./outputs/`).
- `README.md` with setup instructions (CLI and GitHub Desktop) and an explanation of how agents, skills, and `CLAUDE.md` work together.

### Instruction to init a new repo

Set up changelog-based versioning for this repo:

Create CHANGELOG.md in the repo root using the Keep a Changelog format, versioned per SemVer (MAJOR.MINOR.PATCH — MAJOR for breaking/workflow-changing changes, MINOR for new capabilities, PATCH for fixes/tweaks). Seed it with a [1.0.0] (or check if package.json/similar already has a version — use that instead) entry summarizing the current state from recent git history, dated today.
Add a **Version:** x.y.z — see [CHANGELOG.md](CHANGELOG.md) line near the top of README.md, matching the changelog's latest version.
Add a "Versioning" section to this repo's CLAUDE.md (create one if it doesn't exist) that:
Defines what counts as a functional change for this specific repo (be concrete — e.g. "source code, build config, CLI behavior" vs. "docs, fixtures, sample data" — adapt to what this repo actually contains).
Instructs that any commit making a functional change gets a CHANGELOG.md entry (Added/Changed/Fixed/Removed) and a version bump in both CHANGELOG.md and the README header, done proactively as part of the commit — not just when asked.
Ask me what counts as a "functional change" here if it's not obvious from the repo's structure, rather than guessing.

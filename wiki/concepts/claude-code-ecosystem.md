---
type: concept
title: "Claude Code Ecosystem: Skills, Plugins, Hooks & CLAUDE.md"
aliases:
  - "Claude Code skills"
  - "Agent skills"
tags:
  - "wiki/concept"
  - "topic/claude-code"
  - "topic/agent-skills"
sources:
  - "[[raw/2026-10-23-hayatomaruu-2113719510985269442]]"
  - "[[raw/2026-10-25-danikkk_wqs-2114344135415021632]]"
  - "[[raw/2026-09-28-rvaniaaaa-2104602707675718102]]"
source_count: 3
created: 2026-10-26
updated: 2026-10-26
---
# Claude Code Ecosystem: Skills, Plugins, Hooks & CLAUDE.md

The kept sources configure [[wiki/entities/tools/claude-code|Claude Code]] with a project `CLAUDE.md`, **skills** (`.claude/skills/<name>/SKILL.md`), **subagents** (`.claude/agents/`), **hooks**, **plugins/marketplaces**, and [[wiki/entities/tools/model-context-protocol|MCP]] servers.

- **Harness layers** built from CLAUDE.md, a skill, MCP, permissions/hooks, a reviewer subagent, effort levels, and `/goal` ([[raw/2026-10-23-hayatomaruu-2113719510985269442|@hayatomaruu]]; detail in [[wiki/concepts/agent-harness-engineering|Agent harness engineering]]).
- **Second-brain wiring** ([[raw/2026-10-25-danikkk_wqs-2114344135415021632|@danikkk_wqs]]): `.claude/settings.json` hooks run the linter after every edit under `wiki/` and inject a briefing at session start (matchers startup/resume/clear/compact, "so the briefing survives a /clear"); ingest as a skill (`/ingest`); nightly `claude -p` (with a caveat that `--bare` doesn't load hooks/skills/CLAUDE.md and needs an API key).
- **Plugins**: `/plugin marketplace add kepano/obsidian-skills` then `/plugin install obsidian@obsidian-skills`; similar installs for [[wiki/entities/repos/eugeniughelbur-obsidian-second-brain|obsidian-second-brain]]; [[wiki/entities/repos/agricidaniel-claude-obsidian|claude-obsidian]] via `claude --plugin-dir` ([[raw/2026-10-25-danikkk_wqs-2114344135415021632|@danikkk_wqs]]).
- **Agent skills for Obsidian**: [[wiki/entities/repos/kepano-obsidian-skills|kepano/obsidian-skills]] teaches Obsidian's native formats — vendored in this vault.
- **CLAUDE.md as living profile**: written by an interview prompt and maintained by the model ([[raw/2026-09-28-rvaniaaaa-2104602707675718102|@rvaniaaaa]]).

## Sources

- [[raw/2026-10-23-hayatomaruu-2113719510985269442]]
- [[raw/2026-10-25-danikkk_wqs-2114344135415021632]]
- [[raw/2026-09-28-rvaniaaaa-2104602707675718102]]

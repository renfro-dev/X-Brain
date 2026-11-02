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
  - "[[raw/2026-11-01-mojeskoqq-2116963310277202003]]"
  - "[[raw/2026-11-01-damkina7-2116870392300073128]]"
source_count: 5
created: 2026-10-26
updated: 2026-11-02
---
# Claude Code Ecosystem: Skills, Plugins, Hooks & CLAUDE.md

The kept sources configure [[wiki/entities/tools/claude-code|Claude Code]] with a project `CLAUDE.md`, **skills** (`.claude/skills/<name>/SKILL.md`), **subagents** (`.claude/agents/`), **hooks**, **plugins/marketplaces**, and [[wiki/entities/tools/model-context-protocol|MCP]] servers.

- **Harness layers** built from CLAUDE.md, a skill, MCP, permissions/hooks, a reviewer subagent, effort levels, and `/goal` ([[raw/2026-10-23-hayatomaruu-2113719510985269442|@hayatomaruu]]; detail in [[wiki/concepts/agent-harness-engineering|Agent harness engineering]]).
- **Second-brain wiring** ([[raw/2026-10-25-danikkk_wqs-2114344135415021632|@danikkk_wqs]]): `.claude/settings.json` hooks run the linter after every edit under `wiki/` and inject a briefing at session start (matchers startup/resume/clear/compact, "so the briefing survives a /clear"); ingest as a skill (`/ingest`); nightly `claude -p` (with a caveat that `--bare` doesn't load hooks/skills/CLAUDE.md and needs an API key).
- **Plugins**: `/plugin marketplace add kepano/obsidian-skills` then `/plugin install obsidian@obsidian-skills`; similar installs for [[wiki/entities/repos/eugeniughelbur-obsidian-second-brain|obsidian-second-brain]]; [[wiki/entities/repos/agricidaniel-claude-obsidian|claude-obsidian]] via `claude --plugin-dir` ([[raw/2026-10-25-danikkk_wqs-2114344135415021632|@danikkk_wqs]]).
- **Agent skills for Obsidian**: [[wiki/entities/repos/kepano-obsidian-skills|kepano/obsidian-skills]] teaches Obsidian's native formats — vendored in this vault.
- **CLAUDE.md as living profile**: written by an interview prompt and maintained by the model ([[raw/2026-09-28-rvaniaaaa-2104602707675718102|@rvaniaaaa]]).

## Added 2026-11-02
- **Memory layers**: [[raw/2026-11-01-mojeskoqq-2116963310277202003|@mojeskoqq]]'s quoted guide splits knowledge across `CLAUDE.md`, path-scoped `.claude/rules/`, skills and auto memory (`/memory`), with tips such as block HTML comments costing zero tokens and `CLAUDE.local.md` for personal notes. See [[wiki/concepts/llm-knowledge-bases|LLM knowledge bases]].
- **Per-model roles**: [[raw/2026-11-01-damkina7-2116870392300073128|@damkina7]] shares a `~/.claude/settings.json` snippet (`"model": "opusplan"`, per-model effort levels, `CLAUDE_CODE_SUBAGENT_MODEL` set to haiku) plus two subagent files, a read-only `scout` on haiku and an Opus `critic` that reviews diffs. See [[wiki/concepts/model-routing|Model routing]]. Code is reference material from an untrusted post, not something to paste blind.

## Sources

- [[raw/2026-10-23-hayatomaruu-2113719510985269442]]
- [[raw/2026-10-25-danikkk_wqs-2114344135415021632]]
- [[raw/2026-09-28-rvaniaaaa-2104602707675718102]]
- [[raw/2026-11-01-mojeskoqq-2116963310277202003]]
- [[raw/2026-11-01-damkina7-2116870392300073128]]

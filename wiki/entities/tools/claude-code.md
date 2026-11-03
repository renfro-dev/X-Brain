---
type: tool
title: "Claude Code"
aliases:
  - "claude code"
  - "CC"
tags:
  - "wiki/tool"
  - "topic/claude-code"
sources:
  - "[[raw/2026-10-23-hayatomaruu-2113719510985269442]]"
  - "[[raw/2026-10-25-danikkk_wqs-2114344135415021632]]"
  - "[[raw/2026-09-28-rvaniaaaa-2104602707675718102]]"
  - "[[raw/2026-11-01-mojeskoqq-2116963310277202003]]"
  - "[[raw/2026-11-01-damkina7-2116870392300073128]]"
  - "[[raw/2026-11-02-hanakoxbt-2117365616579666418]]"
source_count: 6
created: 2026-10-26
updated: 2026-11-03
---
# Claude Code

Anthropic's agentic coding CLI, the main tool in the kept sources. Features referenced: CLAUDE.md, skills, subagents, hooks (PreToolUse, after-edit, SessionStart), plugins & marketplaces, MCP, `/mcp`, `/permissions`, `/context`, `/agents`, `/goal`, `/rewind`, `/clear`, `claude -p`, effort levels ([[raw/2026-10-23-hayatomaruu-2113719510985269442|@hayatomaruu]], [[raw/2026-10-25-danikkk_wqs-2114344135415021632|@danikkk_wqs]]). [[raw/2026-09-28-rvaniaaaa-2104602707675718102|@rvaniaaaa]]'s prompts target Claude (Desktop) with file-system access.

Concepts: [[wiki/concepts/claude-code-ecosystem|Claude Code ecosystem]], [[wiki/concepts/agent-harness-engineering|Agent harness engineering]].

## Added 2026-11-02
- Memory layers (`CLAUDE.md`, `.claude/rules/`, skills, auto memory) from [[raw/2026-11-01-mojeskoqq-2116963310277202003|@mojeskoqq]] and a per-model settings and subagent setup from [[raw/2026-11-01-damkina7-2116870392300073128|@damkina7]]. See [[wiki/concepts/claude-code-ecosystem|Claude Code ecosystem]].

## Added 2026-11-03

- [[raw/2026-11-02-hanakoxbt-2117365616579666418|@hanakoxbt]] pitches a "9-step loop" (Hanako's Loops and Graphs article) to wrap around Claude Code before letting it touch a repo, and says most people "just type \"fix this bug\"". See [[wiki/concepts/agent-loops-and-graphs|Agent loops & graphs]].

## Sources

- [[raw/2026-10-23-hayatomaruu-2113719510985269442]]
- [[raw/2026-10-25-danikkk_wqs-2114344135415021632]]
- [[raw/2026-09-28-rvaniaaaa-2104602707675718102]]
- [[raw/2026-11-01-mojeskoqq-2116963310277202003]]
- [[raw/2026-11-01-damkina7-2116870392300073128]]
- [[raw/2026-11-02-hanakoxbt-2117365616579666418]]

---
type: concept
title: "MCP & Context Management"
aliases:
  - "Context engineering"
  - "Context budget"
tags:
  - "wiki/concept"
  - "topic/mcp-context"
sources:
  - "[[raw/2026-10-23-hayatomaruu-2113719510985269442]]"
  - "[[raw/2026-10-25-danikkk_wqs-2114344135415021632]]"
source_count: 2
created: 2026-10-26
updated: 2026-10-26
---
# MCP & Context Management

Keeping tools and knowledge from overflowing the context window.

- [[raw/2026-10-23-hayatomaruu-2113719510985269442|@hayatomaruu]] (quoted harness article): add an MCP connection only when it supports a specific task step; tool results "should carry enough information for the next decision"; disable unused servers via `/mcp`; inspect what's loaded with `/context`; keep root CLAUDE.md focused (re-read after compaction) with details in files retrieved when needed.
- [[raw/2026-10-25-danikkk_wqs-2114344135415021632|@danikkk_wqs]]: don't `@import` a big index ("Imports load at launch and cost as much context as pasting the file in"); keep a dozen-line `hot.md`; you only need the Local REST API plugin + an MCP server "to talk to a running Obsidian"; subagents keep bulk ingest out of the main context; auto memory loads only the first 200 lines / 25KB of MEMORY.md.

Related entity: [[wiki/entities/tools/model-context-protocol|Model Context Protocol]].

## Sources

- [[raw/2026-10-23-hayatomaruu-2113719510985269442]]
- [[raw/2026-10-25-danikkk_wqs-2114344135415021632]]

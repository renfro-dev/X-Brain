---
type: concept
title: "Claude Code Built-in Commands (the "15 official commands")"
aliases:
  - "Claude Code slash commands"
  - "/goal /batch /loop"
tags:
  - "wiki/concept"
  - "topic/claude-code"
  - "topic/slash-commands"
  - "topic/agent-loops"
sources:
  - "[[raw/2026-11-08-hanakoxbt-2119538190868775268]]"
source_count: 1
created: 2026-11-09
updated: 2026-11-09
---
# Claude Code Built-in Commands (the "15 official commands")

@hanakoxbt lists 15 built-in [[wiki/entities/tools/claude-code|Claude Code]] commands "most people never type", each linked to code.claude.com docs ([[raw/2026-11-08-hanakoxbt-2119538190868775268|post]]). The list is the author's; the doc pages were not fetched, so descriptions are hers.

## The list (as described by @hanakoxbt)

/goal (keep working until a condition is true), /batch (split a change across parallel agents), /subtask (hand off a side task with full context), /deep-research (cited report), /design (editable artboards), /plan (plan first, edit after approval), /memory (edit CLAUDE.md memory), /compact (free context, keep key decisions), /branch (try another direction), /rewind (roll back to a checkpoint), /mcp (manage tools), /loop (repeat a check while the session runs), /schedule (cloud routines), /simplify (clean up changed code with 4 parallel reviewers), /remote-control (continue from a phone). Her suggested start: /plan → /goal → /simplify.

## Synthesis

The commands map onto vault themes: /goal and /loop are the "check that can fail" from [[wiki/concepts/agent-loops-and-graphs|Loops & graphs]]; /batch and /subtask are graph-style parallelism; /memory and /compact are [[wiki/concepts/mcp-and-context-management|context management]]; /schedule matches [[wiki/concepts/always-on-agent-infrastructure|always-on agents]]. The post ends by pointing to her "Graph Engineering" guide, the same loops-and-graphs article already in the vault. The framing "before you blame Opus 5.5" is hers. See also [[wiki/concepts/claude-code-ecosystem|Claude Code ecosystem]].

## Sources

- [[raw/2026-11-08-hanakoxbt-2119538190868775268]]

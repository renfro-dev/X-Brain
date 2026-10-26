---
type: concept
title: "Multi-Agent Orchestration"
aliases:
  - "Agent orchestration"
  - "Multi-agent systems"
  - "Agent-to-agent"
tags:
  - "wiki/concept"
  - "topic/multi-agent"
sources:
  - "[[raw/2026-10-23-hayatomaruu-2113719510985269442]]"
  - "[[raw/2026-10-24-mardehaym-2113991017506414930]]"
  - "[[raw/2026-10-25-danikkk_wqs-2114344135415021632]]"
source_count: 3
created: 2026-10-26
updated: 2026-10-26
---
# Multi-Agent Orchestration

Coordinating several agents. Thin in the kept sources — three angles:

- [[raw/2026-10-23-hayatomaruu-2113719510985269442|@hayatomaruu]]: "99% of people still hand-roll multi-agent systems and wonder why they break"; the quoted harness article pairs a main agent with a bounded evidence-reviewer subagent (read/search tools only; corrections stay with the main agent).
- [[raw/2026-10-24-mardehaym-2113991017506414930|@mardehaym]]: step six **agent-to-agent** — "Agent A finishes, hands off to Agent B. An LLM sits between them as a quality gate, judging every handoff"; step seven **step functions** — "Agents handle volume. Humans handle exceptions."
- [[raw/2026-10-25-danikkk_wqs-2114344135415021632|@danikkk_wqs]]: for bulk ingest, one subagent per source on a cheaper model (subagents return only a summary), then a separate verifier in a fresh context.

Related: [[wiki/concepts/agent-harness-engineering|Agent harness engineering]], [[wiki/concepts/agentic-org-maturity|Agentic org maturity]].

## Sources

- [[raw/2026-10-23-hayatomaruu-2113719510985269442]]
- [[raw/2026-10-24-mardehaym-2113991017506414930]]
- [[raw/2026-10-25-danikkk_wqs-2114344135415021632]]

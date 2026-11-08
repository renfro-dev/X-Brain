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
  - "[[raw/2026-10-30-hanakoxbt-2116267647100707095]]"
  - "[[raw/2026-10-27-Dhruvkumar16797-2114897217425449463]]"
  - "[[raw/2026-11-01-damkina7-2116870392300073128]]"
  - "[[raw/2026-11-01-suraj_sharma14-2116787322716885503]]"
  - "[[raw/2026-11-06-s4yonnara-2118814330695073907]]"
source_count: 8
created: 2026-10-26
updated: 2026-11-08
---
# Multi-Agent Orchestration

Coordinating several agents. Thin in the kept sources — three angles:

- [[raw/2026-10-23-hayatomaruu-2113719510985269442|@hayatomaruu]]: "99% of people still hand-roll multi-agent systems and wonder why they break"; the quoted harness article pairs a main agent with a bounded evidence-reviewer subagent (read/search tools only; corrections stay with the main agent).
- [[raw/2026-10-24-mardehaym-2113991017506414930|@mardehaym]]: step six **agent-to-agent** — "Agent A finishes, hands off to Agent B. An LLM sits between them as a quality gate, judging every handoff"; step seven **step functions** — "Agents handle volume. Humans handle exceptions."
- [[raw/2026-10-25-danikkk_wqs-2114344135415021632|@danikkk_wqs]]: for bulk ingest, one subagent per source on a cheaper model (subagents return only a summary), then a separate verifier in a fresh context.

Related: [[wiki/concepts/agent-harness-engineering|Agent harness engineering]], [[wiki/concepts/agentic-org-maturity|Agentic org maturity]].

## Added 2026-10-31
- [[raw/2026-10-30-hanakoxbt-2116267647100707095|@hanakoxbt]] (Hanako's "Loops and Graphs" article): give workers isolated contexts, because shared windows make four auditors converge ("four times for one opinion with three echoes"). Use code nodes, not models, for merge/rank/dedupe. See [[wiki/concepts/agent-loops-and-graphs|Agent loops & graphs]].
- [[raw/2026-10-27-Dhruvkumar16797-2114897217425449463|@Dhruvkumar16797]]: relayed Andrew Ng "Graph Engineering" course, from a single agent to full automation.

## Added 2026-11-02
- [[raw/2026-11-01-damkina7-2116870392300073128|@damkina7]]: "Opus thinks. Sonnet builds. The cheap models grind." Opus plans, Sonnet writes code, Haiku scouts, and a critic agent reviews the diff. See [[wiki/concepts/model-routing|Model routing]].
- [[raw/2026-11-01-suraj_sharma14-2116787322716885503|@suraj_sharma14]]'s interview list asks when to pick single versus multi-agent and how an orchestrator splits work between sub-agents. See [[wiki/concepts/agent-system-design-questions|Agent system design questions]].

## Added 2026-11-08
- [[raw/2026-11-06-s4yonnara-2118814330695073907|@s4yonnara]] lists "15 GitHub projects" of ready-made agent teams instead of "building AI agent teams from scratch". The agent-team repos (descriptions are the author's): `serenakeyitan/agent-org-chart` (teams for engineering, marketing, support, sales), `jaredtrichard/grok-factory` (one coordinator delegating to specialists), `simo255/multiBot` (teammates that hand heavy work to coding CLIs), `mKay00/grok-bot-second-brain` (five agents for coordination, memory, research, operations), `Archive228/foreman` (monitors teams, flags stalled tasks, verifies finished work), `YannisKiefer/grokbot-x` (X research and drafting), `function1st/PhoneZero` (phone calls and bookings with approval gates), `mandarwagh9/botroster` (self-hosted teammates with shared files and scheduled tasks), `HAEGONG/grok-bot-profiles` (Spec Writer, Bug Reproducer, PR Producer, PR Verifier), and `galleonlabs/hypergrok-trading-desk` (seven trading-desk agents). The last five links are general trading libraries (cryptofeed, CCXT, Freqtrade, VectorBT, QuantStats), not agent teams.
- His closing advice: "Start with one team and give it a clear job… Give each agent defined responsibilities and approval boundaries." None of the repos were opened or vetted for this vault; treat the list as leads. See [[wiki/entities/tools/grok-bot|Grok Bot]].

## Sources

- [[raw/2026-10-23-hayatomaruu-2113719510985269442]]
- [[raw/2026-10-24-mardehaym-2113991017506414930]]
- [[raw/2026-10-25-danikkk_wqs-2114344135415021632]]
- [[raw/2026-10-30-hanakoxbt-2116267647100707095]]
- [[raw/2026-10-27-Dhruvkumar16797-2114897217425449463]]
- [[raw/2026-11-01-damkina7-2116870392300073128]]
- [[raw/2026-11-01-suraj_sharma14-2116787322716885503]]
- [[raw/2026-11-06-s4yonnara-2118814330695073907]]

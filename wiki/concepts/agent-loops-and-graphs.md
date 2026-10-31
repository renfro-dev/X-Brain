---
type: concept
title: "Agent Loops & Graphs"
aliases:
  - "Loop engineering"
  - "Graph engineering"
  - "Harness → Loop → Graph"
tags:
  - "wiki/concept"
  - "topic/agent-loops"
  - "topic/agent-graphs"
  - "topic/multi-agent"
sources:
  - "[[raw/2026-10-25-m4lkxx-2114338456750997922]]"
  - "[[raw/2026-10-30-hanakoxbt-2116267647100707095]]"
  - "[[raw/2026-10-27-Dhruvkumar16797-2114897217425449463]]"
source_count: 3
created: 2026-10-31
updated: 2026-10-31
---
# Agent Loops & Graphs

A recurring Oct 2026 framing: **Prompts/Chat → Agents → Harness → Loops → Graphs**. The harness gives the agent a place to work, the loop checks a unit of work, the graph decides which units exist. Sits on top of [[wiki/concepts/agent-harness-engineering|Agent harness engineering]].

## Claims
- [[raw/2026-10-25-m4lkxx-2114338456750997922|@m4lkxx]] ("Harness, Loops, Graphs"): "Your agent is not autonomous. You are its loop." The layers "are not a menu, they are a ladder" — each exists because the one below breaks predictably. Levels run from chat (you do all the work) → harness with hands → harness with memory and walls ("The context window is RAM. The harness is the disk"; "A wall is not an instruction") → loop with a check that can fail → loop with convergent feedback (EXPECTED/SAW, FENCE, DEAD ENDS, exit when the same result repeats) → graphs and fleets. "If you cannot write the check, you do not understand the task yet."
- [[raw/2026-10-30-hanakoxbt-2116267647100707095|@hanakoxbt]] quotes Hanako's article "Loops and Graphs…": "A loop makes a unit of work correct without you. A graph decides which units exist at all." "The loop lives inside a node. The graph lives between them." Node types: splitter, worker, code node, gate. Drop fake "and then" edges; give workers isolated contexts; keep a short **correction edge** and a long **learning edge** back to the splitter; return the failing unit, not the batch, capped at three attempts; open gates on **blast radius**, not model confidence. The post's claim that this is a Karpathy prompt isn't backed by the capture.
- [[raw/2026-10-27-Dhruvkumar16797-2114897217425449463|@Dhruvkumar16797]] relays a 2-hour "Graph Engineering" course attributed to [[wiki/entities/people/andrew-ng|Andrew Ng]]: first agent → loop engineering → graph engineering → agents that rewrite themselves → full graph system. "Same model, same tokens, completely different week."

## Synthesis
All three agree that reliability comes from structure, not a better model: a check that can fail (see [[wiki/concepts/verification-and-linting|Verification & linting]]), then a graph that parallelizes independent work ([[wiki/concepts/multi-agent-orchestration|Multi-agent orchestration]]).

## Sources

- [[raw/2026-10-25-m4lkxx-2114338456750997922]]
- [[raw/2026-10-30-hanakoxbt-2116267647100707095]]
- [[raw/2026-10-27-Dhruvkumar16797-2114897217425449463]]

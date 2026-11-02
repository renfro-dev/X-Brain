---
type: concept
title: "Agent Harness Engineering"
aliases:
  - "Harness"
  - "Harness engineering"
  - "Agent harness"
tags:
  - "wiki/concept"
  - "topic/agent-harness"
sources:
  - "[[raw/2026-10-23-hayatomaruu-2113719510985269442]]"
  - "[[raw/2026-10-24-mardehaym-2113991017506414930]]"
  - "[[raw/2026-10-25-m4lkxx-2114338456750997922]]"
  - "[[raw/2026-10-27-Grow_withAI-2115062331227226349]]"
  - "[[raw/2026-11-01-damkina7-2116870392300073128]]"
  - "[[raw/2026-11-01-hayatomaruu-2117003050090938646]]"
  - "[[raw/2026-10-31-LunarResearcher-2116522516915028254]]"
source_count: 7
created: 2026-10-26
updated: 2026-11-02
---
# Agent Harness Engineering

The "harness" is everything around the model — instructions, tools, permissions, state, checks, loops, recovery. Both kept agent sources argue it, not the model, is where reliability (and IP) lives.

## Claims
- [[raw/2026-10-23-hayatomaruu-2113719510985269442|@hayatomaruu]] quotes an unnamed "Anthropic engineer" (promotional framing: "$350K–$950K"): the harness handles loops, context and sandboxing; "brain and hands separated"; runs server-side and resumes from the log after crashes; failure is cheap (retry/replay); yesterday's logs become new memory — "Anthropic calls this 'dreaming'." Unverified relay; the workshop itself isn't captured.
- [[raw/2026-10-24-mardehaym-2113991017506414930|@mardehaym]] (step three of his ladder): "Build evaluation criteria, routing logic, and quality gates before you pick a model… Your harness is your IP and your capex. The model underneath is a commodity… If changing the LLM breaks your system, you built a dependency, not a platform." See [[wiki/concepts/agentic-org-maturity|Agentic org maturity]].

## A concrete 7-layer setup ([[wiki/entities/people/beamnxw|@beamnxw]] article, quoted in [[raw/2026-10-23-hayatomaruu-2113719510985269442|@hayatomaruu]])
"Make Opus 5.5 Finish Long Tasks: A Reusable Harness Engineering Setup" maps harness duties onto [[wiki/entities/tools/claude-code|Claude Code]] features:
1. **Workspace facts** — a focused root `CLAUDE.md`; detail in retrievable files with checked dates.
2. **Saved procedure** — a skill in `.claude/skills/<name>/SKILL.md`; each step has an observable result; keep approval separate from drafting.
3. **Source access** — [[wiki/entities/tools/model-context-protocol|MCP]] connections only where a task step needs them; disable unused servers via `/mcp`.
4. **Action rules** — permission rules at the tool boundary, a `PreToolUse` hook, `.claude/settings.json`; inspect with `/permissions`.
5. **Evidence reviewer** — read-only subagent in `.claude/agents/evidence-reviewer.md` (see [[wiki/concepts/verification-and-linting|Verification & linting]]).
6. **Reasoning effort** — main session at `medium`, reviewer `high`; effort configurable per skill/subagent.
7. **Completion proof** — `/goal` with a completion condition over saved deliverables; `progress.md` for resumption (root CLAUDE.md is re-read after compaction); `/rewind` and git for recovery.

Related: [[wiki/concepts/multi-agent-orchestration|Multi-agent orchestration]], [[wiki/concepts/mcp-and-context-management|MCP & context management]], [[wiki/entities/tools/claude-opus-5-5|Claude Opus 5.5]].

## Added 2026-10-31
- [[raw/2026-10-25-m4lkxx-2114338456750997922|@m4lkxx]]: "Remove the model from your architecture diagram. Everything still on the page is the harness." He prefers "Ten narrow, documented tools… over forty overlapping ones" and says memory and walls live outside the model. Next layer: [[wiki/concepts/agent-loops-and-graphs|Agent loops & graphs]].
- [[raw/2026-10-27-Grow_withAI-2115062331227226349|@Grow_withAI]] reposts the same "Anthropic engineer… harnesses… dreaming" workshop copy as [[raw/2026-10-23-hayatomaruu-2113719510985269442|@hayatomaruu]], nearly verbatim (Steps 1–5 are the same). This is a second relay, not independent confirmation.

## Added 2026-11-02
- [[raw/2026-10-31-LunarResearcher-2116522516915028254|@LunarResearcher]] relays an unnamed "Anthropic engineer" talk ("You're not supposed to prompt Opus 5.5. You're supposed to build a system that prompts itself"; "90% of our engineers have already built these systems"). Unverified, promotional framing. The quoted article, "Harness Engineering: The Complete Guide to Building AI Agents That Don't Fall Apart", argues many agent failures "are environment failures" and that "A prompt changes one attempt. A harness changes every attempt." It starts each task with a **task contract** (outcome, scope, what must not change, evidence of completion, which actions need approval) and says to give the agent "a map, not a manual".
- [[raw/2026-11-01-damkina7-2116870392300073128|@damkina7]] quotes his own article "The Harness Is the Machine: The Claude Opus 5.5 Engineering Manifest" ("The model is only the engine / The harness is the machine"). It lists seven harness jobs (define/contract, select/context, act/tools in isolated git worktrees, remember/state as on-disk receipts, verify/sensors, and more) and claims the same model goes from 18% to 89% completion on a multi-file refactor inside a harness. Those numbers are the author's own claim with no cited benchmark.
- [[raw/2026-11-01-hayatomaruu-2117003050090938646|@hayatomaruu]] (second bookmark from this author) attributes to "Anthropic engineer Andrej Karpathy" the line "Opus 5.5 is just the brain. The /harness is what makes it useful" and pitches smaller models plus tools, graphs and feedback loops. It quotes [[wiki/entities/people/beamnxw|@beamnxw]]'s "Agent Harness Engineering vs. Loop Engineering vs. Graph Engineering", which cites LangChain ("the agent is the model plus the harness") and OpenAI's Agents SDK.

> [!warning] Contradiction
> [[raw/2026-11-01-hayatomaruu-2117003050090938646|@hayatomaruu]] calls Karpathy an "Anthropic engineer", while his own text and [[wiki/entities/people/andrej-karpathy|Karpathy's page]] describe him as ex-OpenAI and ex-Tesla. Treat the quote and the "16-minute breakdown" as unverified.

## Sources

- [[raw/2026-10-23-hayatomaruu-2113719510985269442]]
- [[raw/2026-10-24-mardehaym-2113991017506414930]]
- [[raw/2026-10-25-m4lkxx-2114338456750997922]]
- [[raw/2026-10-27-Grow_withAI-2115062331227226349]]
- [[raw/2026-11-01-damkina7-2116870392300073128]]
- [[raw/2026-11-01-hayatomaruu-2117003050090938646]]
- [[raw/2026-10-31-LunarResearcher-2116522516915028254]]

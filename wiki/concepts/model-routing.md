---
type: concept
title: "Model Routing (Right Model per Job)"
aliases:
  - "Model routing"
  - "Opus plans, Sonnet builds"
tags:
  - "wiki/concept"
  - "topic/model-routing"
  - "topic/claude-code"
sources:
  - "[[raw/2026-11-01-damkina7-2116870392300073128]]"
  - "[[raw/2026-11-01-hayatomaruu-2117003050090938646]]"
source_count: 2
created: 2026-11-02
updated: 2026-11-02
---
# Model Routing (Right Model per Job)

Using different models for different jobs inside one agent setup instead of one big model for everything.

## Claims
- [[raw/2026-11-01-damkina7-2116870392300073128|@damkina7]]: Opus 5.5 "architects every plan and unblocks when stuck", Sonnet 5.5 "writes the production code", Haiku "scouts file paths and line numbers", and a critic agent "tears your diff apart before you merge". He shares a Claude Code settings snippet (`opusplan`, per-model effort, subagent model set to haiku) and two subagent files (`scout`, `critic`). His quoted article frames this as the worker ("hands") on Sonnet in an isolated git worktree and the auditor ("brain") on Opus in a clean context.
- [[raw/2026-11-01-hayatomaruu-2117003050090938646|@hayatomaruu]]: "Give a smaller model the right tools, graphs, and feedback loops" and "Most people keep paying for a bigger model. The real edge is building the loop that makes a smaller one useful." (Attributed to Karpathy; unverified.)

Synthesis: both sources treat the expensive model as planner and reviewer and push routine work to cheaper models, with the harness doing the coordination. Related: [[wiki/concepts/agent-harness-engineering|Agent harness engineering]], [[wiki/concepts/multi-agent-orchestration|Multi-agent orchestration]], [[wiki/entities/tools/claude-opus-5-5|Claude Opus 5.5]].

## Sources

- [[raw/2026-11-01-damkina7-2116870392300073128]]
- [[raw/2026-11-01-hayatomaruu-2117003050090938646]]

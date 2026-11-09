---
type: concept
title: "Company Brain & Agent Cost Control"
aliases:
  - "Company brain"
  - "cheap decision layer"
  - "agent cost control"
tags:
  - "wiki/concept"
  - "topic/company-brain"
  - "topic/agent-cost"
  - "topic/model-routing"
sources:
  - "[[raw/2026-11-08-irongiantXBT-2119484092089762141]]"
source_count: 1
created: 2026-11-09
updated: 2026-11-09
---
# Company Brain & Agent Cost Control

A claim from [[raw/2026-11-08-irongiantXBT-2119484092089762141|@irongiantXBT]] that a team's agent setup gets cheaper and safer when a small, fast "decision" model answers routine yes/no questions and the expensive model is only called for the hard part. All numbers below are the author's, from a promotional 14-page PDF post; none are verified in this vault.

## Claims

- @irongiantXBT's 10 steps ([[raw/2026-11-08-irongiantXBT-2119484092089762141|post]]): Opus 5.5 "thinks", a tool called "jev" "decides" with a typed answer and calibrated probability, and Grok Bot "holds the branch". He claims jev answers in 0.44s for $0.00035 per call, and that about 99% of turns end at a confident answer without escalating.
- He claims the hardest ~1% escalates to Opus 5.5 with 1M context, citing 66.4% on "terminal-bench 4.0", and that every bash call is classified before it runs.
- Cost claims: a Claude bill from $765 to $3 a month; $3.50 a day to judge 10,000 traces, matching a human label on 500 of 500 decisions; cache reads at $0.20 per MTok "20x cheaper" than a fresh load; switching models mid-session costing $5.84 against $3.32 for staying put.
- The post says the architecture was "pulled out of the typesafe and anthropic docs". "jev" is not explained in the post, so what it is remains unknown here.

> [!warning] Unverified / promotional
> The post sells a PDF and a linked article. Benchmark, price and savings figures are the author's only and no method is shown.

## Synthesis

This is the same idea as [[wiki/concepts/model-routing|Model routing]] pushed further: route by confidence, not just by task type, and keep a gate on actions ([[wiki/concepts/verification-and-linting|Verification]]). Related: [[wiki/concepts/agent-harness-engineering|Agent harness engineering]], [[wiki/concepts/mcp-and-context-management|Context management]].

## Sources

- [[raw/2026-11-08-irongiantXBT-2119484092089762141]]

---
type: concept
title: "Agent System Design Questions (Interview Checklist)"
aliases:
  - "AI engineer interview questions"
  - "Agent design checklist"
tags:
  - "wiki/concept"
  - "topic/ai-engineering-interviews"
  - "topic/agent-design"
sources:
  - "[[raw/2026-11-01-suraj_sharma14-2116787322716885503]]"
source_count: 1
created: 2026-11-02
updated: 2026-11-02
---
# Agent System Design Questions (Interview Checklist)

[[raw/2026-11-01-suraj_sharma14-2116787322716885503|@suraj_sharma14]] lists 25 questions he says "come up again and again" in AI engineer interviews. They double as a self-check for anyone building agents. His closing line: "Most candidates can explain an LLM. Very few can design a system around one."

## The questions, grouped (grouping is synthesis)
- **Basics**: chatbot versus agent, how an agent picks a tool, the think-act-observe loop, RAG versus fine-tuning, embeddings and vector databases, small context windows, short- and long-term memory, what MCP is.
- **Architecture**: single versus multi-agent, how an orchestrator splits work, stopping infinite loops.
- **Safety**: guardrails before real tools, where a human approves actions, prompt injection, failed tool calls.
- **Quality and cost**: evaluating whether an agent works, production metrics, debugging wrong answers, reducing hallucinations, token cost, latency.
- **Design exercises**: a flight-booking agent, a customer support agent, what breaks at 1M users, an agent you built and what failed.

Where this vault already has answers: [[wiki/concepts/agent-loops-and-graphs|Loops & graphs]] (looping and stopping rules), [[wiki/concepts/verification-and-linting|Verification]] (evals and evidence), [[wiki/concepts/mcp-and-context-management|MCP & context]], [[wiki/concepts/multi-agent-orchestration|Multi-agent orchestration]], [[wiki/concepts/llm-knowledge-bases|LLM knowledge bases]] (memory).

## Sources

- [[raw/2026-11-01-suraj_sharma14-2116787322716885503]]

---
type: concept
title: "Always-On / Headless Agents"
aliases:
  - "Headless agents"
  - "Background agents"
  - "Scheduled agents"
tags:
  - "wiki/concept"
  - "topic/always-on-agents"
sources:
  - "[[raw/2026-10-24-mardehaym-2113991017506414930]]"
  - "[[raw/2026-10-23-hayatomaruu-2113719510985269442]]"
  - "[[raw/2026-10-25-danikkk_wqs-2114344135415021632]]"
  - "[[raw/2026-09-28-rvaniaaaa-2104602707675718102]]"
  - "[[raw/2026-11-06-s4yonnara-2118814330695073907]]"
source_count: 5
created: 2026-10-26
updated: 2026-11-08
---
# Always-On / Headless Agents

Agents that keep working without the user at the keyboard.

- **Go headless** — step four of [[raw/2026-10-24-mardehaym-2113991017506414930|@mardehaym]]'s ladder: "Host every automation outside a laptop. It fires on schedule, on conditions, without a human logging in at 9 AM"; companies stall moving from "script on my desktop" to "service that runs on its own."
- **Server-side, resumable runs** — the harness in [[raw/2026-10-23-hayatomaruu-2113719510985269442|@hayatomaruu]] "runs server-side, resumes from the log after crashes"; the quoted article keeps `progress.md` so the next session can recover.
- **Scheduled knowledge upkeep** — nightly `claude -p` via cron/CI or Claude Desktop's Schedule tab ([[raw/2026-10-25-danikkk_wqs-2114344135415021632|@danikkk_wqs]]); a daily compilation task that writes you a brief ([[raw/2026-09-28-rvaniaaaa-2104602707675718102|@rvaniaaaa]]; needs Claude Desktop on a paid plan, per the author).

Related: [[wiki/concepts/agentic-org-maturity|Agentic org maturity]], [[wiki/concepts/llm-knowledge-bases|LLM knowledge bases]].

## Added 2026-11-08
- [[raw/2026-11-06-s4yonnara-2118814330695073907|@s4yonnara]] quotes his own X Article "Grok Bot for Beginners", which describes [[wiki/entities/tools/grok-bot|Grok Bot]] as "an AI agent with its own computer in the cloud" that keeps working after you close your laptop. His advice: treat a bot like a hire with a brief (what it owns, what good looks like, where it must stop), start with one bot, pick a frequent, cheap-to-check first task, and do a dry run by asking what it *would* do first. Pricing and launch details in the article are the author's claims.

## Sources

- [[raw/2026-10-24-mardehaym-2113991017506414930]]
- [[raw/2026-10-23-hayatomaruu-2113719510985269442]]
- [[raw/2026-10-25-danikkk_wqs-2114344135415021632]]
- [[raw/2026-09-28-rvaniaaaa-2104602707675718102]]
- [[raw/2026-11-06-s4yonnara-2118814330695073907]]

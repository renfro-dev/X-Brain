---
type: concept
title: "Verification, Linting & Evidence"
aliases:
  - "Wiki lint"
  - "Evidence reviewer"
  - "Health checks"
tags:
  - "wiki/concept"
  - "topic/verification"
sources:
  - "[[raw/2026-09-28-rvaniaaaa-2104602707675718102]]"
  - "[[raw/2026-10-25-danikkk_wqs-2114344135415021632]]"
  - "[[raw/2026-10-23-hayatomaruu-2113719510985269442]]"
source_count: 3
created: 2026-10-26
updated: 2026-10-26
---
# Verification, Linting & Evidence

LLM-maintained artifacts need checks the model can't talk its way past.

- [[raw/2026-09-28-rvaniaaaa-2104602707675718102|@rvaniaaaa]]: a **lint** prompt that hunts contradictions, stale claims, orphan pages, missing concepts — "report only, fix nothing"; run it on a schedule because bad sources spread.
- [[raw/2026-10-25-danikkk_wqs-2114344135415021632|@danikkk_wqs]]: planted a false sentence ("Bush invented hypertext in 1941"); an LLM asked to "check the wiki for errors" would let it through, but a ~95-line non-AI script (`brain.py`) caught it. Checks: every page has title/sources/updated; listed sources exist; every link resolves; no orphans or leftover TODOs; raw files changed after ingest are flagged with stale pages listed; **every quoted claim exists word-for-word in the cited raw file**. Wired as a Claude Code hook after every edit under `wiki/`. Caveat: "checks structure and quotes, not truth."
- [[raw/2026-10-23-hayatomaruu-2113719510985269442|@hayatomaruu]] (quoted @beamnxw article): a read-only **evidence-reviewer** subagent whose findings connect each claim to an opened source; unresolved verdicts name the missing evidence; `/goal` completion defined in terms of saved deliverables and verification results.

This vault's lint rules (in `CLAUDE.md`) borrow from these. Related: [[wiki/concepts/llm-knowledge-bases|LLM knowledge bases]], [[wiki/concepts/agent-harness-engineering|Agent harness engineering]].

## Sources

- [[raw/2026-09-28-rvaniaaaa-2104602707675718102]]
- [[raw/2026-10-25-danikkk_wqs-2114344135415021632]]
- [[raw/2026-10-23-hayatomaruu-2113719510985269442]]

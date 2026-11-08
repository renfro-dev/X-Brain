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
  - "[[raw/2026-10-25-m4lkxx-2114338456750997922]]"
  - "[[raw/2026-10-30-hanakoxbt-2116267647100707095]]"
  - "[[raw/2026-11-01-damkina7-2116870392300073128]]"
  - "[[raw/2026-10-31-LunarResearcher-2116522516915028254]]"
  - "[[raw/2026-11-06-undefinedKi-2118825045644513583]]"
source_count: 8
created: 2026-10-26
updated: 2026-11-08
---
# Verification, Linting & Evidence

LLM-maintained artifacts need checks the model can't talk its way past.

- [[raw/2026-09-28-rvaniaaaa-2104602707675718102|@rvaniaaaa]]: a **lint** prompt that hunts contradictions, stale claims, orphan pages, missing concepts — "report only, fix nothing"; run it on a schedule because bad sources spread.
- [[raw/2026-10-25-danikkk_wqs-2114344135415021632|@danikkk_wqs]]: planted a false sentence ("Bush invented hypertext in 1941"); an LLM asked to "check the wiki for errors" would let it through, but a ~95-line non-AI script (`brain.py`) caught it. Checks: every page has title/sources/updated; listed sources exist; every link resolves; no orphans or leftover TODOs; raw files changed after ingest are flagged with stale pages listed; **every quoted claim exists word-for-word in the cited raw file**. Wired as a Claude Code hook after every edit under `wiki/`. Caveat: "checks structure and quotes, not truth."
- [[raw/2026-10-23-hayatomaruu-2113719510985269442|@hayatomaruu]] (quoted @beamnxw article): a read-only **evidence-reviewer** subagent whose findings connect each claim to an opened source; unresolved verdicts name the missing evidence; `/goal` completion defined in terms of saved deliverables and verification results.

This vault's lint rules (in `CLAUDE.md`) borrow from these. Related: [[wiki/concepts/llm-knowledge-bases|LLM knowledge bases]], [[wiki/concepts/agent-harness-engineering|Agent harness engineering]].

## Added 2026-10-31
- [[raw/2026-10-25-m4lkxx-2114338456750997922|@m4lkxx]]: "A check is only as strong as the weakest thing it accepts as proof". Watch the check fail once before the fix, and "Writing the check is writing the spec."
- [[raw/2026-10-30-hanakoxbt-2116267647100707095|@hanakoxbt]]: write the condition first so a program could evaluate it, and don't treat a second model's review as the check ("Two optimists agreeing"). "Absence of an error is not evidence of correctness."

## Added 2026-11-02
- [[raw/2026-11-01-damkina7-2116870392300073128|@damkina7]]'s harness rule: no diff merges without sensors returning exit code 0 (syntax parse, strict typecheck such as `pyright` or `tsc --noEmit`, bounded tests), and a cold-context Opus review of the raw diff and test receipts before commit.
- [[raw/2026-10-31-LunarResearcher-2116522516915028254|@LunarResearcher]]'s quoted guide lists "It claimed success without running the checks" as a typical environment failure and asks every task contract to name "What evidence proves completion?"

## Added 2026-11-08
- [[raw/2026-11-06-undefinedKi-2118825045644513583|@undefinedKi]] (relaying Addy Osmani): run tests via a hook after every file edit so the agent sees failures right away; add the rule "never skip or delete a test to make it pass"; and have a fresh chat review the changes against `plan.md`, because the same chat shouldn't grade its own work. This matches the separate-reviewer idea earlier on this page.

## Sources

- [[raw/2026-09-28-rvaniaaaa-2104602707675718102]]
- [[raw/2026-10-25-danikkk_wqs-2114344135415021632]]
- [[raw/2026-10-23-hayatomaruu-2113719510985269442]]
- [[raw/2026-10-25-m4lkxx-2114338456750997922]]
- [[raw/2026-10-30-hanakoxbt-2116267647100707095]]
- [[raw/2026-11-01-damkina7-2116870392300073128]]
- [[raw/2026-10-31-LunarResearcher-2116522516915028254]]
- [[raw/2026-11-06-undefinedKi-2118825045644513583]]

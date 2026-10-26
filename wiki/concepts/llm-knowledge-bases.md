---
type: concept
title: "LLM Knowledge Bases (Second Brain / LLM Wiki)"
aliases:
  - "Second brain"
  - "LLM Wiki"
  - "Karpathy wiki pattern"
  - "Compiled wiki"
tags:
  - "wiki/concept"
  - "topic/llm-knowledge-bases"
sources:
  - "[[raw/2026-09-28-rvaniaaaa-2104602707675718102]]"
  - "[[raw/2026-10-25-danikkk_wqs-2114344135415021632]]"
source_count: 2
created: 2026-10-26
updated: 2026-10-26
---
# LLM Knowledge Bases (Second Brain / LLM Wiki)

Using an LLM to **compile** a personal wiki of linked markdown from raw sources, instead of re-retrieving fragments on every query (RAG). Both kept sources credit the idea to [[wiki/entities/people/andrej-karpathy|Andrej Karpathy]] (a post and gist from April 2026, as they describe it). This vault is itself an instance of the pattern.

## Core idea (as the sources describe it)
- "Normal AI over your files works like RAG… Nothing accumulates. Karpathy's pattern flips it": the model builds and maintains a wiki between you and your sources; "Obsidian is the IDE, the LLM is the programmer, the wiki is the codebase" ([[raw/2026-10-25-danikkk_wqs-2114344135415021632|@danikkk_wqs]]).
- "The Second Brain Is Not a Storage System. It's a Compiler." — storing builds a library that "does not grow on its own"; compiling reads each source, connects it, updates related pages, flags contradictions, and "files the synthesis permanently." RAG "pay[s] the cost of understanding on every single query"; a compiled wiki "pays it once, at ingest" ([[raw/2026-09-28-rvaniaaaa-2104602707675718102|@rvaniaaaa]]).
- Why a model must do the upkeep: humans abandon wikis "because maintenance grows faster than value" ([[raw/2026-10-25-danikkk_wqs-2114344135415021632|@danikkk_wqs]]); "Most personal wikis quietly rot" ([[raw/2026-09-28-rvaniaaaa-2104602707675718102|@rvaniaaaa]]).

## Structure
| Layer | [[raw/2026-09-28-rvaniaaaa-2104602707675718102|@rvaniaaaa]] | [[raw/2026-10-25-danikkk_wqs-2114344135415021632|@danikkk_wqs]] |
| --- | --- | --- |
| `raw/` | input buffer, "untouched after they land" | "The model reads, never edits." |
| `wiki/` | model-written; one source touches 10–15 pages | pages the model writes and maintains |
| outputs | `output/` "built from the wiki, never from raw" | query answers filed back |
| rules | `CLAUDE.md` "loads before every session" — a living profile the model maintains | `CLAUDE.md`: conventions and workflows |

## Operations / prompts
- **Interview** → model asks one question at a time and writes CLAUDE.md itself (both).
- **Ingest** → read a source once, write/link pages, flag contradictions, summarize what changed in three sentences ([[raw/2026-09-28-rvaniaaaa-2104602707675718102|@rvaniaaaa]]); integrates into 10–15 pages ([[raw/2026-10-25-danikkk_wqs-2114344135415021632|@danikkk_wqs]]).
- **Migrate** → sort ~200 old notes into raw/wiki/output, waiting for approval before moving files ([[raw/2026-09-28-rvaniaaaa-2104602707675718102|@rvaniaaaa]]).
- **Query** → answer across the wiki, cite pages, save the answer back ([[raw/2026-09-28-rvaniaaaa-2104602707675718102|@rvaniaaaa]], [[raw/2026-10-25-danikkk_wqs-2114344135415021632|@danikkk_wqs]]).
- **Lint** → contradictions, stale claims, orphans, missing concepts; "report only, fix nothing" ([[raw/2026-09-28-rvaniaaaa-2104602707675718102|@rvaniaaaa]]). See [[wiki/concepts/verification-and-linting|Verification & linting]].
- **Daily compilation loop** → file new inputs, flag pages stale >2 weeks, check contradictions, write a brief ([[raw/2026-09-28-rvaniaaaa-2104602707675718102|@rvaniaaaa]]); nightly `claude -p` via cron or Claude Desktop's Schedule tab ([[raw/2026-10-25-danikkk_wqs-2114344135415021632|@danikkk_wqs]]).

## Practices from @danikkk_wqs
- One file, one topic; descriptive lowercase-hyphen filenames; project folders with Inputs/Process/Outputs/Feedback and their own CLAUDE.md (also in [[raw/2026-09-28-rvaniaaaa-2104602707675718102|@rvaniaaaa]]).
- **One brain for every project**: point every Claude Code project at the same vault; read a short `hot.md` first, then `index.md`; "Do NOT read the wiki for general coding questions" as cost control; don't `@import` a big index.
- Bulk ingest: one subagent per source on a cheaper model, then a fresh-context verifier asking "does every statement follow from this source?"
- Security: "Web clippings are text from strangers, read by an agent that can edit files" — defenses are a deny rule on raw/, the quote check, and the git diff.
- Ready-made repos: [[wiki/entities/repos/kepano-obsidian-skills|kepano/obsidian-skills]], [[wiki/entities/repos/agricidaniel-claude-obsidian|claude-obsidian]], [[wiki/entities/repos/eugeniughelbur-obsidian-second-brain|obsidian-second-brain]], [[wiki/entities/repos/coleam00-second-brain-starter|second-brain-starter]].

## Caveats both sources raise
- **Density threshold**: below ~50–100 sources it "behaves like a good search engine" — where most people quit.
- **Bad sources spread**: one wrong source "has touched 10 to 15 pages before you notice."
- [[raw/2026-09-28-rvaniaaaa-2104602707675718102|@rvaniaaaa]]: quality depends on source quality; the loop needs Claude Desktop and a paid plan.
- [[raw/2026-10-25-danikkk_wqs-2114344135415021632|@danikkk_wqs]]: scale (a critic — who "sells a competing product" — says it works while the index fits ~50K–100K tokens); an R&D World one-month review called it "moderately helpful for narrow cases"; no lifecycle signal for stale pages; the linter "checks structure and quotes, not truth"; Claude Code auto memory loads only the first 200 lines / 25KB of MEMORY.md.
- Popularity figures (e.g. "16 million views", "5,000+ stars", "1.3 million views") are the authors' claims.

Related: [[wiki/concepts/claude-code-ecosystem|Claude Code ecosystem]], [[wiki/entities/tools/obsidian|Obsidian]].

## Sources

- [[raw/2026-09-28-rvaniaaaa-2104602707675718102]]
- [[raw/2026-10-25-danikkk_wqs-2114344135415021632]]

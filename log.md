---
type: log
---
# log

Append-only. Newest entries at the bottom. Format: `## YYYY-MM-DD — <action>`.

## 2026-10-26 — backfill (initial build)

- Created vault locally at `/workspace/x-brain` (git, branch `main`, no remote). Schema in `CLAUDE.md` = `AGENTS.md`.
- Vendored kepano/obsidian-skills @ 3ccff53 into `.skills/obsidian-skills/` (MIT, LICENSE kept).
- Read all bookmarks for @renfrodotdev (user id 924000909960519680) via X API `get_users_bookmarks` (read-only); `get_users_bookmark_folders` returned no folders → `folder: unfiled`. `bookmarked_on` = 2026-10-26 for all (X doesn't expose bookmark time).
- Full text: note_tweet for long posts; quoted X Articles (plain_text + code blocks); self-threads expanded via `search_posts_all` + `get_posts_by_ids`. API JSON saved in `state/api_snapshots/2026-10-26/`.
- API quirk: large `max_results` returned a single page with no `next_token`; `max_results` 10 paginated normally to the same ids. Use small pages on future syncs.
- Added `index.md`, `bookmarks.base`, `maps/concept-map.canvas`, `state/sync_state.json`, `outputs/README.md`.

## 2026-10-26 — prune (at Joshua's request, before first push)

- Joshua asked to keep only 4 bookmarks. **19 bookmarks were pruned**; their ids, handles and URLs are listed in `state/exclusions.json` (reason: "pruned by Joshua before first push"). Daily sync treats excluded ids as seen and never re-captures them.
- Removed their `raw/` notes and stripped their data from `state/api_snapshots/2026-10-26/` (non-kept posts, includes and thread files removed).
- Rebuilt the wiki from the 4 kept sources only: 26 pages — 8 concepts, 7 people, 4 tools, 4 repos, 3 summaries. Pages without a kept source were deleted; remaining pages trimmed to what the kept sources support.
- Rewrote git history (fresh orphan branch replacing `main`, reflog expired, gc pruned) so pruned content is in no commit.

## 2026-10-31 — sync (+6 bookmarks)

- Read bookmarks for @renfrodotdev via `get_users_bookmarks` (max_results 10, read-only). Page 1 had 6 new ids and 4 already captured. Page 2 held only excluded ids, so paging stopped there. No excluded ids were captured.
- New raw notes: @m4lkxx (article), @gregisenberg (quote), @hanakoxbt (quote, with a quoted X Article), @guilleflorvs, @Dhruvkumar16797 and @Grow_withAI (posts). API JSON saved in `state/api_snapshots/2026-10-31/`.
- New wiki pages: concepts `agent-loops-and-graphs` and `ai-native-services`; people `m4lkxx`, `gregisenberg`, `hanakoxbt`, `guilleflorvs`, `dhruvkumar16797`, `grow-withai` and `andrew-ng`; summary `digest-ai-services-business`.
- Extended: `agent-harness-engineering`, `multi-agent-orchestration`, `verification-and-linting`, `andrej-karpathy`, `claude-opus-5-5`, `digest-agents-and-harnesses`, `vault-digest`.
- Flagged as unverified: @hanakoxbt's "Karpathy prompt" attribution, the @Dhruvkumar16797 "Andrew Ng course" attribution, and @Grow_withAI as a near-duplicate of the @hayatomaruu relay.
- Updated `index.md`, `state/sync_state.json`, `bookmarks.base` (new "Agents: loops & graphs" view) and `maps/concept-map.canvas` (2 new concept nodes).

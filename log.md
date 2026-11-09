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

## 2026-11-02 — sync (+5 bookmarks)

- Read bookmarks for @renfrodotdev via `get_users_bookmarks` (max_results 10, read-only). Page 1 had 5 new ids followed by already-captured ids, so paging stopped. `get_users_bookmark_folders` still returns no folders. No excluded ids were captured.
- New raw notes: @mojeskoqq, @damkina7, @hayatomaruu and @LunarResearcher (quotes, each with a full quoted X Article and code blocks) and @suraj_sharma14 (post). Added post_ids: 2116963310277202003, 2116787322716885503, 2116870392300073128, 2117003050090938646, 2116522516915028254. API JSON saved in `state/api_snapshots/2026-11-02/`.
- New wiki pages: concepts `model-routing` and `agent-system-design-questions`; people `mojeskoqq`, `damkina7`, `lunarresearcher` and `suraj-sharma14`.
- Extended: `agent-harness-engineering`, `agent-loops-and-graphs`, `llm-knowledge-bases`, `claude-code-ecosystem`, `multi-agent-orchestration`, `verification-and-linting`, `hayatomaruu`, `beamnxw`, `andrej-karpathy`, `claude-code`, `claude-opus-5-5`, `obsidian`, and the three affected digests.
- Flagged as unverified: the Karpathy quotes in @mojeskoqq and @hayatomaruu (the latter also calls him an "Anthropic engineer", recorded as a contradiction), the "Anthropic engineer" relay in @LunarResearcher, and @damkina7's 18% versus 89% completion figures.
- Updated `index.md`, `state/sync_state.json` and `maps/concept-map.canvas` (2 new concept nodes).

## 2026-11-03 — sync (+2 bookmarks)

- Read bookmarks for @renfrodotdev via `get_users_bookmarks` (max_results 10, read-only). Page 1 had 2 new ids followed by already-captured ids, so paging stopped. `get_users_bookmark_folders` still returns no folders. No excluded ids were captured.
- New raw notes: @hanakoxbt (quote of the already-captured "Loops and Graphs" X Article; quoted text reproduced from the 2026-10-31 snapshot because the API omitted it from includes) and @renfrodotdev (Joshua's own post sharing a YouTube video on how Karpathy uses LLMs; link and title only). Added post_ids: 2117365616579666418, 2117273838153298014. API JSON saved in `state/api_snapshots/2026-11-03/`.
- Extended: `agent-loops-and-graphs`, `hanakoxbt`, `andrej-karpathy`, `claude-code`, `digest-agents-and-harnesses`, `vault-digest`.
- Flagged as unverified: @hanakoxbt's "Anthropic paper" label (contradiction callout against the earlier "Karpathy prompt" label for the same article) and the YouTube title's framing of Karpathy.
- Updated `index.md` and `state/sync_state.json`.

## 2026-11-08 — sync (+2 bookmarks)

- Read bookmarks for @renfrodotdev via `get_users_bookmarks` (max_results 10, read-only). Page 1 had 2 new ids followed by already-captured ids, so paging stopped. No excluded ids were captured.
- New raw notes: @s4yonnara (quote; list of 15 GitHub agent-team and trading repos, quoting his X Article "Grok Bot for Beginners") and @undefinedKi (quote; seven harness habits relayed from Addy Osmani, quoting @gippp69's sponsored Viktor article). Added post_ids: 2118814330695073907, 2118825045644513583. API JSON saved in `state/api_snapshots/2026-11-08/`.
- New wiki pages: tool `grok-bot`; people `s4yonnara` and `undefinedki`.
- Extended: `multi-agent-orchestration`, `agent-harness-engineering`, `verification-and-linting`, `claude-code-ecosystem`, `always-on-agent-infrastructure`, `claude-code`, `digest-agents-and-harnesses`, `vault-digest`.
- Flagged as unverified or promotional: the relayed Addy Osmani quote, the @gippp69 article (marked "In partnership with Viktor", promo code), and the repo descriptions and Grok Bot pricing in @s4yonnara's post and article.
- Rebuilt `index.md` from the vault (also restores the two 2026-11-03 raw notes to the raw list) and updated `state/sync_state.json`.

## 2026-11-09 — sync (+3 bookmarks)

- Bookmarks for @renfrodotdev were read with `get_users_bookmarks` (max_results 10, read-only). Page 1 had 3 new ids followed by already-captured ids, so paging stopped. Full text and quoted X Articles were fetched with `get_posts_by_ids`. No excluded ids were captured.
- New raw notes (quotes, each with a full quoted X Article and code blocks): @irongiantXBT (company-brain PDF with Grok Bot and "jev", quoting his "10 Bots That Work While You Sleep"), @monokern (first 6 Grok Bot bots, quoting his REA reverse-engineering course) and @hanakoxbt (15 official Claude Code commands, quoting her Loops and Graphs article). Added post_ids: 2119484092089762141, 2119446181231067489, 2119538190868775268. Raw filenames use the UTC post date (2026-11-08); `bookmarked_on` is 2026-11-09. API JSON saved in `state/api_snapshots/2026-11-09/`.
- New wiki pages: concepts `company-brain-and-agent-cost`, `agent-bot-catalogs` and `claude-code-slash-commands`; people `irongiantxbt` and `monokern`; repo `morluto-rea`.
- Extended: `grok-bot`, `claude-code`, `claude-opus-5-5`, `claude-code-ecosystem`, `multi-agent-orchestration`, `agent-loops-and-graphs`, `model-routing`, `verification-and-linting`, `agent-harness-engineering`, `hanakoxbt`, `digest-agents-and-harnesses`, `vault-digest`.
- Flagged as unverified or promotional: @irongiantXBT's cost, latency, benchmark and accuracy figures (PDF teaser) and the unexplained "jev"; @monokern's "110,000 GitHub stars" claim for morluto/rea and the 4-hours-a-day claim; the bot-list descriptions and SpaceXSI attributions; @hanakoxbt's command descriptions (doc pages not fetched). Three videos are captured as media links only.
- Updated `index.md`, `state/sync_state.json` and `maps/concept-map.canvas` (3 new concept nodes).

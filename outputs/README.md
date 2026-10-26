---
type: readme
---
# outputs/

Filed answers, briefs, comparisons, and slide decks produced by querying the wiki.

- Name files `YYYY-MM-DD-<slug>.md` (Marp slides: `YYYY-MM-DD-<slug>.slides.md`).
- Frontmatter: `type: output`, `question`, `created`, `sources` (wiki pages and raw notes cited).
- Build outputs from `wiki/` pages; open the cited `raw/` notes for exact quotes. Cite raw notes as `[[raw/<file>]]`.
- Log each new output in `log.md`. Outputs that add durable knowledge may be folded back into wiki pages (cite the output).

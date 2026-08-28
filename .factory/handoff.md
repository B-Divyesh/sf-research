# Research handoff

Completed the `research-devtools-data-0827-181601-2` work order without building a product.

- Added exactly 12 `RESEARCHED` devtools-data opportunity briefs to `briefs/research-devtools-data-0827-181601-2.json`.
- Added the required one-line-per-brief summary to `briefs/research-devtools-data-0827-181601-2.md`.
- Evidence URLs were fetched from HN Algolia item endpoints and GitHub public issue pages; each brief has two evidence records dated 2025–2026.
- No pre-existing `briefs/*.json` or `.factory/backlog-slugs.txt` was present, so there were no existing ideas/slugs to exclude.

Verify with:

```bash
jq 'length' briefs/research-devtools-data-0827-181601-2.json
jq -e 'all(.[]; .territory == "devtools-data" and (.evidence | length >= 2))' briefs/research-devtools-data-0827-181601-2.json
```

Nothing remains to build or deploy for this research-only work order.
## research-small-business-0828-134517-5

Completed research only; no product was built.

- Added `briefs/research-small-business-0828-134517-5.json` with exactly 12 RESEARCHED small-business opportunity briefs.
- Each brief has two distinct, fetched public evidence URLs (one HN thread and one GitHub issue); no evidence URL is reused within the file.
- Added the one-line-per-brief summary in `briefs/research-small-business-0828-134517-5.md`.
- Validated the JSON with `jq empty`; no runtime/build step is applicable.
- Left the pre-existing unrelated `graphify-out/cache/stat-index.json` modification untouched.

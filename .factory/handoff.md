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
# Research handoff: education

Completed work order `research-education-0828-092927-3`.

- Added `briefs/research-education-0828-092927-3.json`: a valid JSON array of exactly 12 researched education opportunity briefs.
- Added `briefs/research-education-0828-092927-3.md`: one-line why-now summary for each brief.
- Evidence was researched from Hacker News (Algolia item API), Anki/Obsidian/Logseq public forums, and Stack Exchange public API. The selected 24 evidence URLs are all unique across briefs and each brief has two independently sourced records.
- No product was built and no product state files were created, as requested.

Verification:

```bash
jq -e 'length == 12 and ([.[].slug] | length == (unique | length)) and ([.[].evidence[].url] | length == (unique | length))' briefs/research-education-0828-092927-3.json
git diff --check
```

The existing unrelated modification `graphify-out/cache/stat-index.json` was intentionally left untouched and is not part of this work order's commit.

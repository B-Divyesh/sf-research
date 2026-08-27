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
Research work order `research-education-0827-183753-3` is complete.

- Added `briefs/research-education-0827-183753-3.json`: exactly 12 researched education opportunity briefs, each with two unique, fetched public evidence URLs from two sites.
- Added `briefs/research-education-0827-183753-3.md`: one-line why-now summary for every brief.
- No product was built and no runtime verification is needed. Validate the deliverable with `jq empty briefs/research-education-0827-183753-3.json`.
- The pre-existing modification to `graphify-out/cache/stat-index.json` was left untouched.

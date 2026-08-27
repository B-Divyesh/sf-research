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
# Research handoff — research-hobbies-0827-231123-15

Created `briefs/research-hobbies-0827-231123-15.json` with exactly 12 researched hobby-product opportunity briefs and `briefs/research-hobbies-0827-231123-15.md` with the requested one-line summaries.

The JSON is data only; verify with `jq empty briefs/research-hobbies-0827-231123-15.json`. Evidence URLs were fetched directly from GitHub issue APIs and Stack Exchange APIs/pages; each brief uses two distinct, non-reused evidence URLs from those two source families. No product was built.

Existing unrelated `graphify-out/cache/stat-index.json` worktree modification was preserved.

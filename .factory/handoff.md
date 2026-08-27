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
Completed research work order `research-health-home-0827-231050-12`.

- Added `briefs/research-health-home-0827-231050-12.json` with exactly 12 non-overlapping utilities briefs, each with two fetched, unique public evidence URLs from separate sites.
- Added `briefs/research-health-home-0827-231050-12.md` with the requested one-line-per-brief summary.
- No product was built. Validate the deliverable with `python3 -m json.tool briefs/research-health-home-0827-231050-12.json >/dev/null`.
- An unrelated pre-existing modification remains at `graphify-out/cache/stat-index.json`; it was not included in this work order commit.

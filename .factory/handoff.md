# Research handoff — research-installables-0828-134538-7

Completed the installables research work order without building a product.

- `briefs/research-installables-0828-134538-7.json` contains exactly 12 researched briefs, each with two unique public evidence URLs (one Hacker News discussion and one GitHub issue) from 2025-2026.
- `briefs/research-installables-0828-134538-7.md` is the required one-line-per-brief summary.
- `products/*.json` contains parked product-state stubs for the twelve candidates; no repositories or deployments were created.

Verification run:

```bash
jq 'length == 12 and ([.[].evidence[].url] | length == unique | length)' briefs/research-installables-0828-134538-7.json
for f in products/*.json; do jq empty "$f"; done
```

All selected evidence URLs were fetched during research. Existing devtools-data briefs were read before selecting ideas; no slug or core idea was duplicated. The unrelated pre-existing modification to `graphify-out/cache/stat-index.json` was left untouched.

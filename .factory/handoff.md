# Research handoff — devtools-data

Completed work order `research-devtools-data-0827-183507-2`.

- Added `briefs/research-devtools-data-0827-183507-2.json`: 12 `RESEARCHED` devtools/data opportunity briefs, each with two unique public evidence URLs (one HN Algolia thread and one GitHub issue).
- Added `briefs/research-devtools-data-0827-183507-2.md`: one-line why-now summary for each brief.
- Research included 18 HN query variations, 37 GitHub issue-search variations, and reading 30 distinct HN discussions plus the 12 cited GitHub issues.

Verification:

```bash
node -e "const a=require('./briefs/research-devtools-data-0827-183507-2.json'); console.log(a.length, new Set(a.flatMap(x=>x.evidence.map(e=>e.url))).size)"
```

Expected output is `12 24`.

No product was built. An unrelated pre-existing modification remains at `graphify-out/cache/stat-index.json`; it was not included in this work.

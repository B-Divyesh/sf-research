# Research handoff

Completed `research-installables-0828-093012-7` without building a product.

- Added exactly 12 `RESEARCHED` installable-software opportunity briefs in `briefs/research-installables-0828-093012-7.json` and a one-line summary in the matching Markdown file.
- Added one parked product-state record per brief under `products/`; no repositories, releases, or deployments were created.
- Each brief contains two fetched, distinct evidence URLs. The research covered 15 HN search phrasings and opened 25 HN threads, then cross-checked candidates against public GitHub issue pages and Lobsters where useful.
- Existing research was reviewed and overlapping slugs/ideas were avoided. The unrelated pre-existing modification `graphify-out/cache/stat-index.json` was left untouched.

Verify with:

```bash
python3 -c 'import json; d=json.load(open("briefs/research-installables-0828-093012-7.json")); assert len(d)==12; assert len({x["slug"] for x in d})==12; assert len({e["url"] for x in d for e in x["evidence"]})==24'
git status --short
```

Nothing remains to build or deploy for this research-only work order.

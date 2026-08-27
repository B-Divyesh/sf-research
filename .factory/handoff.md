# Research handoff

Completed the `research-utilities-0827-231008-8` work order without building a product.

- Added exactly 12 `RESEARCHED` utilities opportunity briefs to `briefs/research-utilities-0827-231008-8.json`.
- Added the required one-line-per-brief summary to `briefs/research-utilities-0827-231008-8.md`.
- Read 31 distinct HN threads and more than 20 public GitHub issues/feature requests after a 20-query search pass; each selected brief cites two fetched, distinct 2025–26 URLs from HN and GitHub. No evidence URL is reused between briefs.
- Reviewed the existing brief JSON and found no `.factory/backlog-slugs.txt`; the new slugs do not duplicate the existing portfolio.
- Left the unrelated pre-existing modification to `graphify-out/cache/stat-index.json` untouched.

Verify with:

```bash
jq 'length' briefs/research-utilities-0827-231008-8.json
jq -e 'length == 12 and all(.[]; .territory == "utilities" and (.evidence | length >= 2) and .state == "RESEARCHED")' briefs/research-utilities-0827-231008-8.json
```

Nothing remains to build or deploy for this research-only work order.

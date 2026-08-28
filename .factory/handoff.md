# Research handoff: utilities

Completed work order `research-utilities-0828-134421-0`; no product was built or deployed.

- Added exactly 12 `RESEARCHED` utilities opportunity briefs in `briefs/research-utilities-0828-134421-0.json`.
- Added the required one-line-per-brief summary in `briefs/research-utilities-0828-134421-0.md`.
- Added a `PARKED` product-state record for each researched slug under `products/`, ready for a later admission decision.
- Read the existing devtools research brief and checked for `.factory/backlog-slugs.txt` before selecting slugs; no utilities ideas or slug list existed to duplicate.
- Research used 40+ varied public-source searches and read 60+ distinct Hacker News/Algolia threads. The final evidence records are 24 unique, actually fetched 2025–2026 thread URLs; no evidence URL is shared between briefs.

Verify:

```bash
jq -e 'length == 12 and all(.[]; .territory == "utilities" and (.evidence | length >= 2) and .state == "RESEARCHED")' briefs/research-utilities-0828-134421-0.json
jq -e '([.[].evidence[].url] | length) == ([.[].evidence[].url] | unique | length)' briefs/research-utilities-0828-134421-0.json
```

No build, deployment, credentials, or follow-up work remains. The pre-existing `graphify-out/cache/stat-index.json` modification was left untouched.

# Research handoff: health-home

Completed the research work order and committed the deliverables.

- `briefs/research-health-home-0827-183525-4.json` contains exactly 12 `RESEARCHED` local-first utility opportunities, each with two unique fetched public evidence URLs from different sites.
- `briefs/research-health-home-0827-183525-4.md` is the requested one-line-per-brief summary.

Verification run:

```bash
jq 'length' briefs/research-health-home-0827-183525-4.json
jq -e 'length == 12 and all(.[]; (.evidence|length) >= 2 and (.territory == "utilities") and (.state == "RESEARCHED"))' briefs/research-health-home-0827-183525-4.json
jq -r '.[].evidence[].url' briefs/research-health-home-0827-183525-4.json | sort | uniq -d
git diff --check
```

No product was built and no product state files were created. The pre-existing modification to `graphify-out/cache/stat-index.json` was left untouched.

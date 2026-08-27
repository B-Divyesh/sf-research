# Research handoff

Completed `research-small-business-0827-231101-13` without building a product.

- Added `briefs/research-small-business-0827-231101-13.json`: exactly 12 `RESEARCHED` utility briefs, each with two distinct directly fetched public evidence URLs (HN plus GitHub), with no evidence URL shared between briefs.
- Added `briefs/research-small-business-0827-231101-13.md`: one why-now line per brief.
- Surveyed the existing brief and backlog slug file (not present); none of the new slugs overlap the existing devtools portfolio.
- Research coverage: 54 differently phrased HN/GitHub/Lobsters searches, 26 fetched HN item threads, and directly fetched GitHub issue records. GitHub global issue search was rate-limited, so repository issue-list and individual issue endpoints were used instead. Reddit was tried twice and blocked.

Verification:

```bash
jq 'length == 12 and all(.[]; .state == "RESEARCHED" and (.evidence | length >= 2))' briefs/research-small-business-0827-231101-13.json
jq -r '.[].evidence[].url' briefs/research-small-business-0827-231101-13.json | sort | uniq -d
```

No product source, deployment, or generated assets were added. The pre-existing unrelated modification at `graphify-out/cache/stat-index.json` was intentionally left untouched and uncommitted.

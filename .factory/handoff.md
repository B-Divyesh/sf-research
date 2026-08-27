# Research handoff

Completed the `research-utilities-0827-230839-0` work order without building a product.

- Added exactly 12 `RESEARCHED` utilities opportunity briefs to `briefs/research-utilities-0827-230839-0.json`.
- Added the requested one-line-per-brief summary to `briefs/research-utilities-0827-230839-0.md`.
- Ran 35 varied public-source searches (including the requested request-language variants) and read 29 distinct HN item threads plus 18 GitHub issue pages. Each selected brief has a 2025–2026 HN discussion and a different public GitHub issue URL; no evidence URL is reused across briefs.
- Checked existing `briefs/*.json` and the available backlog-slug location before choosing slugs. The pre-existing devtools-data briefs were preserved and no utility slug duplicates them.
- Validated that the JSON is an array of exactly 12 briefs, all with `territory: utilities`, `state: RESEARCHED`, two evidence records, two source domains per brief, unique slugs, and globally unique evidence URLs.

Verify with:

```bash
jq -e 'length == 12 and all(.[]; .territory == "utilities" and .state == "RESEARCHED" and (.evidence | length >= 2))' briefs/research-utilities-0827-230839-0.json
jq -r '.[].evidence[].url' briefs/research-utilities-0827-230839-0.json | sort | uniq -d
git diff --check
```

Nothing remains to build or deploy for this research-only work order.

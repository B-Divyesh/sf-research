# Research handoff: health-home

Completed research-only work order `research-health-home-0828-092939-4`.

- Added `briefs/research-health-home-0828-092939-4.json`: exactly 12 `RESEARCHED` opportunity briefs in the requested schema, each with two distinct fetched public evidence URLs (one HN discussion object and one GitHub issue).
- Added `briefs/research-health-home-0828-092939-4.md`: one-line why-now summary per brief.
- Evidence gathering covered 20 varied Hacker News query phrasings, 20 GitHub query phrasings/repository searches, Lobsters searches, and 28 fetched HN thread objects plus cited GitHub issue objects. Reddit was attempted once per selected subreddit and returned public 403 responses.

Verification run:

```bash
jq -e 'length == 12 and (map(.slug) | unique | length == 12) and (map(.evidence | length) | all(. >= 2)) and (([.[] | .evidence[] | .url]) as $u | ($u | length) == ($u | unique | length))' briefs/research-health-home-0828-092939-4.json
git diff --check
```

No product was built. The pre-existing modification to `graphify-out/cache/stat-index.json` was left untouched.

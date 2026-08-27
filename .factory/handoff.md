# Research handoff: health-home

Completed the research work order without building a product. The committed artifacts are:

- `briefs/research-health-home-0827-183803-4.json` — exactly 12 schema-complete opportunity briefs.
- `briefs/research-health-home-0827-183803-4.md` — one-line rationale per brief.

Research coverage: more than 15 distinct public-source search queries were run, Reddit was tried twice and was blocked, and more than 25 distinct 2025–26 Hacker News/GitHub threads/issues were fetched and read. Each of the 12 briefs cites two unique evidence URLs; no URL is reused by another brief, and every brief spans Hacker News plus GitHub.

Verification: run `jq 'length == 12 and ([.[].slug] | unique | length == 12)' briefs/research-health-home-0827-183803-4.json` and `jq -e 'all(.[]; (.evidence | length >= 2) and .state == "RESEARCHED")' briefs/research-health-home-0827-183803-4.json`.

No product state files or implementation were created, as requested. The pre-existing modification to `graphify-out/cache/stat-index.json` was left untouched.

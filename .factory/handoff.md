# Research handoff: utilities

Completed the utilities research work order without building a product.

- Added `briefs/research-utilities-0827-231134-16.json`: exactly 12 `RESEARCHED` opportunity briefs, each with two unique, fetched public evidence threads (Hacker News via its Algolia item API and Software Recommendations Stack Exchange).
- Added `briefs/research-utilities-0827-231134-16.md`: one-line why-now summary for every brief.
- Avoided collisions with the existing devtools backlog and did not modify the pre-existing `graphify-out/cache/stat-index.json` worktree change.

Verification: run `jq 'length == 12 and all(.[]; .territory == "utilities" and (.evidence | length >= 2))' briefs/research-utilities-0827-231134-16.json`.

Research notes: 15+ HN query variants were run; 26 HN item threads and selected Stack Exchange question bodies were fetched and read. GitHub search was rate-limited and Reddit rejected its public endpoint, so neither was used as evidence.

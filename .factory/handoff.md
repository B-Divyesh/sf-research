# Research handoff

Completed work order `research-utilities-0827-183726-0`.

- Added `briefs/research-utilities-0827-183726-0.json` with exactly 12 utility opportunity briefs, each citing two unique public sources that were directly fetched.
- Added `briefs/research-utilities-0827-183726-0.md` with one concise why-now line per brief.
- Reviewed the existing research JSON and checked `.factory/backlog-slugs.txt` (not present); no existing slug was reused.
- Research included 15 varied search queries and direct reading of 25 distinct HN threads, plus direct verification of cited GitHub issues.

Verification: `python3 -m json.tool briefs/research-utilities-0827-183726-0.json >/dev/null` and a short schema/count check can be run locally. No product was built and no external services require configuration.

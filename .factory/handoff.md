# Research handoff: utilities

Created `briefs/research-utilities-0827-183450-0.json` with exactly 12 researched utility opportunity briefs and `briefs/research-utilities-0827-183450-0.md` with a one-line summary for each.

Research validation: ran 15+ varied HN search queries and fetched/read 25 distinct public threads/issues (13 HN item threads and 12 GitHub issues). Each brief has exactly two unique evidence URLs: one HN thread and one GitHub issue; no evidence URL is reused between briefs.

Verification: `node -e 'JSON.parse(require("fs").readFileSync("briefs/research-utilities-0827-183450-0.json")); console.log("valid JSON")'`.

No product implementation or product-state files were created. The pre-existing unrelated modification to `graphify-out/cache/stat-index.json` was preserved.

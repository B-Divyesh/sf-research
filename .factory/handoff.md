# Research handoff: devtools-data

Completed work order `research-devtools-data-0827-183744-2`.

- Added `briefs/research-devtools-data-0827-183744-2.json` with exactly 12 `devtools-data` opportunity briefs.
- Added `briefs/research-devtools-data-0827-183744-2.md` with one why-now line per brief.
- Research covered 20 Hacker News discovery queries, 15 Lobsters discovery queries, and targeted GitHub issue searches. I read 28 HN threads and 20 GitHub issue pages directly before writing.
- Every brief has two unique, directly fetched evidence URLs: one Hacker News discussion and one GitHub issue. No evidence URL is shared between briefs.

Verification:

```bash
python3 - <<'PY'
import json
briefs = json.load(open('briefs/research-devtools-data-0827-183744-2.json'))
assert len(briefs) == 12
assert len({e['url'] for b in briefs for e in b['evidence']}) == 24
print('validated', len(briefs), 'briefs')
PY
```

No product was built. An unrelated pre-existing modification to `graphify-out/cache/stat-index.json` was left untouched and is not part of this work.

# Research handoff: education

Completed work order `research-education-0828-070127-3`.

- Added `briefs/research-education-0828-070127-3.json` with exactly 12 `RESEARCHED` opportunity briefs.
- Added `briefs/research-education-0828-070127-3.md` with one why-now line for each brief.
- Surveyed 15+ varied public-source search queries and read 26 distinct HN threads/GitHub issues. Every brief has two fetched public evidence URLs from two sites, and all 24 evidence URLs are unique across the array.
- No product was built and no product state files were created; this work order is research-only.

Verify with:

```bash
python3 -m json.tool briefs/research-education-0828-070127-3.json >/dev/null
python3 - <<'PY'
import json
d = json.load(open('briefs/research-education-0828-070127-3.json'))
u = [e['url'] for x in d for e in x['evidence']]
assert len(d) == 12 and len(u) == len(set(u)) == 24
PY
```

The pre-existing modification to `graphify-out/cache/stat-index.json` was left untouched.

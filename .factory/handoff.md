# Research handoff: small-business

Completed work order `research-small-business-0827-183533-5`.

- Added `briefs/research-small-business-0827-183533-5.json`: exactly 12 `RESEARCHED` small-business utility briefs.
- Added `briefs/research-small-business-0827-183533-5.md`: one-line why-now summary for each brief.
- Read the existing briefs and checked for an existing backlog-slug file before selection. There were no existing small-business slugs to avoid.
- Research covered 20 HN query phrasings and 45 individually fetched 2025–26 HN/GitHub threads/issues. The final briefs use 24 non-reused, directly fetched evidence URLs; each has one HN and one GitHub source.

Verification:

```bash
python3 - <<'PY'
import json
d=json.load(open('briefs/research-small-business-0827-183533-5.json'))
assert len(d) == 12
assert len({x['slug'] for x in d}) == 12
urls=[e['url'] for x in d for e in x['evidence']]
assert len(urls) == len(set(urls)) == 24
print('valid:', len(d), 'briefs')
PY
```

No product was built and no product-state files were created: this work order requested research artifacts only. A pre-existing unrelated modification, `graphify-out/cache/stat-index.json`, was intentionally left uncommitted.

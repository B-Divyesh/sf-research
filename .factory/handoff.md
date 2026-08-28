## Research handoff: research-installables-0828-070214-7

Completed installable-software research only; no product was built.

- Added `briefs/research-installables-0828-070214-7.json`: exactly 12 `RESEARCHED` opportunity briefs, each with two distinct, fetched public-source URLs (Hacker News/Algolia and GitHub), scoped v1/non-goals, constraints, and a falsifiable success metric.
- Added `briefs/research-installables-0828-070214-7.md`: one-line portfolio summary per brief.
- Research coverage included 15 varied Hacker News search queries, 25 individually fetched HN threads, and public issue data from installable-software projects. Existing brief slugs were checked before drafting.

Verification:

```bash
python3 - <<'PY'
import json
briefs = json.load(open('briefs/research-installables-0828-070214-7.json'))
assert len(briefs) == 12
assert len({b['slug'] for b in briefs}) == 12
assert all(len(b['evidence']) >= 2 for b in briefs)
print('valid briefs:', len(briefs))
PY
git diff --check
```

The pre-existing modification to `graphify-out/cache/stat-index.json` was left untouched.

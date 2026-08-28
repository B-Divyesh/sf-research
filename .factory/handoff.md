# Research handoff

Completed the `research-utilities-0828-092851-0` work order without building a product.

- Added exactly 12 `RESEARCHED` utilities opportunity briefs to `briefs/research-utilities-0828-092851-0.json`.
- Added the required one-line-per-brief summary to `briefs/research-utilities-0828-092851-0.md`.
- Read the existing devtools research and checked `.factory/backlog-slugs.txt`; none of the new utility slugs duplicate that backlog.
- Ran breadth searches across HN, GitHub, Lobsters, and Reddit (Reddit was unreachable), then fetched and read 30+ individual HN/Lobsters/GitHub threads. Each final brief has two actually fetched, non-reused evidence URLs from two distinct sites.

Verify with:

```bash
python3 -m json.tool briefs/research-utilities-0828-092851-0.json >/dev/null
python3 - <<'PY'
import json
d = json.load(open('briefs/research-utilities-0828-092851-0.json'))
assert len(d) == 12
urls = [e['url'] for brief in d for e in brief['evidence']]
assert len(urls) == len(set(urls)) == 24
assert all(len({e['url'].split('/')[2] for e in brief['evidence']}) >= 2 for brief in d)
PY
```

Nothing remains to build or deploy for this research-only work order.

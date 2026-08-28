# Research handoff

Created and committed the venture research work order artifacts:

- `briefs/research-ventures-0828-174526-0.json` — exactly 12 `RESEARCHED`, `venture`-scale opportunity briefs.
- `briefs/research-ventures-0828-174526-0.md` — one-line rationale per brief.

Research verification performed: 15+ distinct search queries and 27 directly fetched 2025–2026 public HN threads/GitHub issues. Every brief has a unique evidence URL set with sources from at least two sites; no product was built.

Validate with:

```bash
jq -e 'length == 12 and ([.[].evidence[].url] | length == (unique | length))' briefs/research-ventures-0828-174526-0.json
```

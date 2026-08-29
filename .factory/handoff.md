# Catalogue curation handoff

Created the 514-product `curation.json` and its companion `curation.md`.

- The live `/products.json` ledger supplied the current 514 slugs; all have one shelf, valid kind, interest rating, editorial reason, plain-language `why`, and no more than three tags.
- The catalogue has eight store-style shelves. The 47 releases added since the earlier draft were classified and rated; stale template reasons were replaced.
- Exactly 12 RELEASED feature pages were checked with `curl`. Every URL returned HTTP 200 and exposed a relevant page title.
- `curation.md` records the 12 editorial picks and five first-screen copy fixes for the next perfection loop.

Verify with:

```bash
jq '{products:(.products|length), featured:([.products[]|select(.featured)]|length)}' curation.json
jq -e '[.products[] | select((.why|length) > 110 or (.tags|length) > 3)] | length == 0' curation.json
jq -e '[.products[].interest] | group_by(.) | map({rating: .[0], count: length})' curation.json
```

No product software was built or changed. The existing `graphify-out/cache/stat-index.json` worktree modification was left untouched.

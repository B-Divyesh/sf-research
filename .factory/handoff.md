# Catalogue curation handoff

Updated the Hello Factory catalogue for the 635-product inventory.

- `curation.json` has eight store-style shelves, one curation record per supplied slug, and exactly 12 featured products.
- The old list’s eight retired records were removed and its twelve current omissions were added.
- Placeholder descriptions that only said “Use [product name]” were replaced with plain task descriptions.
- The featured URLs were fetched on 2026-09-01; every one returned HTTP 200 and is in `RELEASED` state.
- `curation.md` records the featured editorial choices and five first-screen copy problems for the repair loop.

Verify with:

```sh
jq -e '(.products | length == 635) and ([.products[] | select(.featured)] | length == 12)' curation.json
jq -e '([.products[] | select((.why | length) > 110 or (.tags | length) > 3)] | length == 0)' curation.json
```

No build is required: this is a research and curation repository. The pre-existing change in `graphify-out/cache/stat-index.json` was intentionally left uncommitted.

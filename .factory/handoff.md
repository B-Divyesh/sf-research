# Curation handoff

Updated and committed-ready `curation.json` and `curation.md` for the 652-product Hello Factory catalogue.

- Reconciled the previous 642-entry file against the live `products.json` feed and curated all 652 current releases.
- Kept eight store-style shelves and supplied one valid curation record for every live product.
- There are exactly 12 featured picks. Each feature URL was checked with `curl` on 2 September 2026; every one returned HTTP 200 and a clear page title.
- `curation.md` gives the editorial reasons for each feature and identifies five first screens needing copy work.

Verify with:

```sh
node - <<'NODE'
const c = require('./curation.json');
console.log({ products: c.products.length, featured: c.products.filter(p => p.featured).length });
NODE
```

Expected: `{ products: 652, featured: 12 }`.

The pre-existing `graphify-out/cache/stat-index.json` modification was left untouched.

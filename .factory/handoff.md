# Curation handoff

Updated `curation.json` and `curation.md` for the 661-product Hello Factory catalogue.

- Reconciled the prior curation against the live `https://hello-factory.sociobot.in/products.json` feed and curated all 661 current releases. Eight retired slugs were removed and thirteen current releases were assessed and added.
- Kept eight store-style shelves and supplied one valid curation record for every live product.
- There are exactly 12 featured picks. Each feature URL was checked with `curl` on 2 September 2026 and returned HTTP 200. Floorplan Text and Kitchen Table were rendered in Chromium to confirm their first screens.
- `curation.md` gives the editorial reasons for each feature and identifies five first screens needing copy work.

Verify with:

```sh
node - <<'NODE'
const c = require('./curation.json');
console.log({ products: c.products.length, featured: c.products.filter(p => p.featured).length });
NODE
```

Expected: `{ products: 661, featured: 12 }`.

The pre-existing `graphify-out/cache/stat-index.json` modification was left untouched.

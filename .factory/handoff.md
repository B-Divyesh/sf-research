# Catalogue curation handoff

## Done

- Curated all 497 supplied live products into eight store-style shelves.
- Added 98 releases missing from the prior catalogue and removed ten entries absent from the current source list.
- Rated every listing, kept every catalogue line under 110 characters, and selected exactly 12 featured products.
- Checked every featured URL with curl. All returned HTTP 200 and are marked RELEASED.
- Wrote the featured rationale and five first-screen copy fixes in `curation.md`.

## Verify

Run:

```bash
jq empty curation.json
node - <<'NODE'
const c = require('./curation.json');
console.log(c.products.length, c.categories.length, c.products.filter(p => p.featured).length);
NODE
```

Expected output: `497 8 12`.

## Left

No build or deploy is required for this research repository. The five repair targets in `curation.md` are recommendations for the product perfection loop.

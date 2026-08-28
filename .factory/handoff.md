# Catalogue curation handoff

## Done

- Curated all 409 live products into eight store-style shelves.
- Added the 42 newly indexed releases and removed nine no-longer-live entries.
- Rated every release, kept all `why` lines below 110 characters, and selected exactly 12 features.
- Checked each featured URL with `curl`; all returned HTTP 200 and are in `RELEASED` state.
- Wrote the feature rationale and five first-screen copy fixes in `curation.md`.

## Verify

Run:

```bash
jq empty curation.json
node -e 'const d=require("./curation.json"); console.log(d.products.length, d.categories.length, d.products.filter(p => p.featured).length)'
```

Expected output: `409 8 12`.

## Left

The 12 feature URLs were checked with curl. No build or deploy is required for this research repository.

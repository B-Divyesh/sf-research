# Catalogue curation handoff

Created and committed `curation.json` and `curation.md` for all 376 live products.

Verification performed:

- `jq` confirms 376 product records, eight shelves, exactly 12 featured products, valid kinds, and `why` lines no longer than 110 characters.
- The 12 featured URLs were fetched with `curl`; each returned HTTP 200 and a legible title/first-screen description.
- Ratings are conservative: 48 five-star entries (12.8%) and 60 four-star entries (16.0%).

There is no build step for this research repository. Inspect the curated data with:

```sh
jq '.products | length' curation.json
jq '[.products[] | select(.featured)] | length' curation.json
```

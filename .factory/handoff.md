# Curation handoff

Created and committed `curation.json` and `curation.md` for the 639-product Hello Factory catalogue.

- The catalogue has eight store-style categories and one complete curation record per live product.
- There are exactly 12 featured, released picks. Each was checked with `curl` on 2 September 2026 and returned HTTP 200 with a recognisable first-screen job.
- `curation.md` records the featured editorial choices and five first screens that need copy work.

Verify with:

```sh
node -e "const c=require('./curation.json'); console.log(c.products.length, c.products.filter(p=>p.featured).length)"
```

This prints `639 12`.

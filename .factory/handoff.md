# Curation handoff

Updated `curation.json` and `curation.md` for the 640-product Hello Factory catalogue.

- The catalogue has eight store-style categories and one complete curation record per current product in the live `products.json` feed.
- Ten new live products were rated and shelved; nine retired products were removed.
- There are exactly 12 featured, released picks. Each was checked with `curl` on 2 September 2026 and returned HTTP 200 with a recognisable first-screen job.
- `curation.md` records the featured editorial choices and five first screens that need copy work.

Verify with:

```sh
node -e "const c=require('./curation.json'); console.log(c.products.length, c.products.filter(p=>p.featured).length)"
```

This prints `640 12`.

No further work is left in this research repository.

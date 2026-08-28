# Catalogue curation handoff

Created and committed the 500-product `curation.json` and the companion `curation.md`.

- The catalogue uses eight store shelves and every live product has one kind, shelf, interest rating, reason, plain-language `why` line, and up to three tags.
- The live product feed was reconciled before writing. Fifteen new live releases were added and twelve no-longer-live entries were removed.
- Exactly 12 featured releases remain. Each featured URL was opened with `curl`; all returned HTTP 200 and exposed a clear title and description on the first screen.
- `curation.md` lists the featured editorial rationale and five first screens that should be improved next.

Verify with:

```bash
jq '{products:(.products|length), featured:([.products[]|select(.featured)]|length)}' curation.json
jq -e '[.products[] | select((.why|length) > 110 or (.tags|length) > 3)] | length == 0' curation.json
```

No product software was built or changed.

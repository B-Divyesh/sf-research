# Catalogue curation handoff

Created `curation.json` for 631 products across eight store-style shelves and `curation.md` with the 12 featured picks plus five first-screen copy issues.

The featured pages were checked with `curl`; all returned HTTP 200. The featured list contains exactly 12 released, product-like picks. Practice tools and scorekeepers were kept out of `game` unless they are games in their own right.

Verify the data with:

```sh
jq '{products:(.products|length),featured:([.products[]|select(.featured)|.slug])}' curation.json
jq -e '([.products[]|select(.featured)]|length == 12) and ([.products[]|select((.why|length)>110)]|length == 0)' curation.json
```

No application build is needed; this repository only contains the research and curation artefacts.

The pre-existing `graphify-out/cache/stat-index.json` worktree change was left untouched.

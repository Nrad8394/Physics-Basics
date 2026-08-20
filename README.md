# Physics Basics

A classical-mechanics refresher, built as a local MkDocs textbook. Nine
chapters from units to gravitation, each with diagrams, worked examples,
common pitfalls, and practice problems with collapsible answers.

## Read it

Two ways:

**Live site with search (recommended):**

```
pip install -r requirements.txt
mkdocs serve
```

then open http://127.0.0.1:8000

**No server:** open `site/index.html` directly in a browser (search won't
work from `file://`, everything else does). Rebuild after editing with
`mkdocs build`.

## Layout

- `docs/` — the chapters (markdown) and `docs/img/` figures
- `mkdocs.yml` — site config and navigation
- `site/` — built HTML (generated, not committed)

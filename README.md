# bostrot.com

The company page of Bostrot Inh. Eric Trenkel — served by GitHub Pages from
this repo's `gh-pages` branch.

**There is no site source here.** Everything (template, styles, fonts, data
pipeline) lives in [bostrot/portfolio-v2](https://github.com/bostrot/portfolio-v2),
which builds two sites from one codebase and publishes them together on every
deploy:

- `dist/` → [erictrenkel.com](https://erictrenkel.com) (Pages via Actions there)
- `dist-bostrot/` → force-pushed to this repo's `gh-pages` branch via a deploy key

To change the site, edit `templates/bostrot.html` (or the shared assets) in
portfolio-v2 — the next push or daily data refresh deploys both domains.

# bostrot.com

Deploy shim for [bostrot.com](https://bostrot.com) — the company page of
Bostrot Inh. Eric Trenkel.

**There is no site source here.** Everything (template, styles, fonts, data
pipeline) lives in [bostrot/portfolio-v2](https://github.com/bostrot/portfolio-v2),
which builds two sites from one codebase:

- `dist/` → [erictrenkel.com](https://erictrenkel.com) (deployed by that repo)
- `dist-bostrot/` → [bostrot.com](https://bostrot.com) (deployed by this repo)

The [workflow](.github/workflows/deploy.yml) checks out portfolio-v2, runs its
build, and publishes `dist-bostrot/` to this repo's GitHub Pages. It runs daily
after portfolio-v2's data refresh, on manual dispatch, and on push.

To change the site, edit `templates/bostrot.html` (or the shared assets) in
portfolio-v2. The next scheduled run picks it up automatically — or trigger
"Build & Deploy bostrot.com" manually for an instant update.

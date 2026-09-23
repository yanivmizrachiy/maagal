# Provenance — maagal (circle workbook)

Extracted 2026-09-23. Pedagogical content is byte-identical to the sources below; only the path changes listed under **Transforms** were made.

| Target | Source |
|---|---|
| `/` (index.html, manifest.json, page-1..101.html, styles.css, a4-utilization.css, source/**) | `yanivmizrachiy/razpages@c8fe7bde7ee19215b5593f9379c3db2f0c846538:workbooks/circle/` |
| `vendor/mathjax/`, `vendor/fonts/` | `yanivmizrachiy/razpages@c8fe7bde7ee19215b5593f9379c3db2f0c846538:vendor/` |
| `styles/a4-base.css`, `styles/pages/עמוד-196..205.css`, `styles/topics/bbb-geometry8.css` | `yanivmizrachiy/razpages@c8fe7bde7ee19215b5593f9379c3db2f0c846538:styles/` |

Canonical choice: razpages `workbooks/circle/manifest.json` declares `sourceOfTruth: true`, 101 pages (consolidated 2026-08-18, commit 38ae6b3). Its `source/original-88/` is byte-identical to `smartschool-hebrew-voice-notes@760f64e82dc6f309c67324df100399532f89bc8f:circle/page-*.html`.

## Transforms
- `page-*.html` (loader shell): `'../../'+v` → `v` — BBB pages' `vendor/` and `styles/` now resolve inside this repo.
- `index.html`: link "כל החוברות" `../index.html` → https://yanivmizrachiy.github.io/razpages/workbooks/index.html
- Not carried: `qa.mjs` / `scripts/qa-circle-canonical.mjs` (checks razpages-only files such as CLAUDE.md and workbooks/manifest.json).

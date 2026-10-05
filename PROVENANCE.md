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

## Circle-improvement pass (branch `improve-circle-work`, 2026-10-05)

### "שאלות מתוך תוכנית הלימודים" — real BBB questions (pages 74–83)
Every question below is the **actual** question from BBB (`geometry8/topics/t01_circle.py`,
commit `ad12425c6b2e1d4dac84030a5cd865c2b03d3804`), rendered byte-for-byte into
`source/bbb/עמוד-196..205.html` and served at maagal pages 74–83. No question here was
invented, rewritten, or "inspired by" — only the minimal corrections listed afterwards.
All ten sit under the single chapter heading **"שאלות מתוך תוכנית הלימודים"**
(SSOT: `manifest.json` stage `enrichment`, pages 74–83), split into the source's own
sub-chapters: א "המעגל וחלקיו" (74–75) and ב "היקף מעגל ושטחו" (76–83).

| maagal page | source file | BBB question (identifying text) |
|---|---|---|
| 74 | `source/bbb/עמוד-196.html` | חוט/יתד/עיפרון — הגדרת המעגל כאוסף הנקודות במרחק קבוע; + מעגל r=5 במערכת צירים |
| 75 | `source/bbb/עמוד-197.html` | נתון קוטר → מהו אורך הרדיוס ומהם שיעורי מרכז המעגל |
| 76 | `source/bbb/עמוד-198.html` | תומר מדד רדיוס גלגל 30 ס״מ → חשבו היקף (π≈3.14) |
| 77 | `source/bbb/עמוד-199.html` | משושה משוכלל חסום במעגל — זוויות המשולשים והיקף המשושה |
| 78 | `source/bbb/עמוד-200.html` | אצטדיון (ריבוע 144 מ״ר + שני חצאי עיגול); שלושה ריבועים חופפים עם עיגולים משיקים |
| 79 | `source/bbb/עמוד-201.html` | ריבוע ABCD עם עיגול חסום (r=6) — היקף ריבוע ויחס שטחים |
| 80 | `source/bbb/עמוד-202.html` | מלבן + חצאי/רבעי עיגול — השוואת היקפים ושטחים של שתי צורות |
| 81 | `source/bbb/עמוד-203.html` | הגלגל הענק (London Eye) — גובה מרכז M מעל המים והיקף הגלגל |
| 82 | `source/bbb/עמוד-204.html` | פארק המזרקה — חלקים 1–3 (שטח בריכה, שטח טיילת כהפרש עיגולים) |
| 83 | `source/bbb/עמוד-205.html` | פארק המזרקה — חלקים 4–5 (הכפלת רדיוס ויחסי שטחים; אתגר תקציב −30%) |

### Minimal corrections to the BBB pages (content essence preserved)
- **Heading** (all 10 `source/bbb/עמוד-196..205.html`): page-title `גאומטריה לכיתה ח'` → `שאלות מתוך תוכנית הלימודים`.
- **עמוד-200.html (page 78)** — math fix: the "three congruent squares" multiple-choice had **no correct option** (the grey area is `π·s²/4` in all three figures, i.e. equal). Added the missing correct option **"בכל האיורים השטח שווה"**. Verified no A4 clipping after the addition.
- **עמוד-204.html / עמוד-205.html (pages 82–83)**: the fountain-park task is one problem split across two A4 pages; its part labels were renumbered to be continuous and self-consistent (`6,7,8` → `1,2,3` on p82; `9,10` → `4,5` on p83). The "גליל וחרוט" chapter-bar on עמוד-205 is kept (the loader uses it as the page-83 trim boundary) but its cylinder/cone questions are **not** served — page 83 carries circle content only (verified: no גליל/חרוט text leaks).

### Canonical language (SSOT) + wording consistency
- Added `canonicalLanguage` to `manifest.json` (the SSOT) with the four required statements:
  כל קוטר הוא מיתר אך לא כל מיתר הוא קוטר · אורך רדיוס הוא אורך חצי קוטר ·
  מרכז המעגל נמצא תמיד באמצע כל קוטר · קוטר הוא המיתר הארוך ביותר במעגל.
- `source/original-88/page-4.html` (page 4 "קוטר"): added a compact "הדגשה" note carrying the four statements verbatim. Page re-verified: no A4 overflow, all four present.
- Page-wording audit against the four statements (pages mentioning מיתר/רדיוס/קוטר: 3, 4, 8, 10, 21/g8-06): all already consistent — no contradictions, no edits needed.

### Other circle corrections
- `source/original-88/page-50.html` (page 53) & `page-51.html` (page 54): fixed regex artifact `r=x−$1` → `r=x−1`.
- `source/targilim/g8-06.html` (page 21): moved the chord segment endpoints onto the circle (center (130,88), r=55) so the "מיתר" is drawn correctly.
- `source/targilim/g8-01.html` (page 43): title `עיגול — …` → `מעגל ועיגול — …` for precision.

### Mobile (viewer) — `index.html`
- Added a phone-width fit (`@media(max-width:760px)`): the viewer measures the real `.a4-page` inside the iframe and scales it to the pane width (absolute `left:0` + `transform-origin:top left`), so the full A4 page is visible with **no horizontal scroll**, on both CSS systems (original `styles.css` and `styles/a4-base.css`). Desktop and print are untouched (fit resets above 760px).

## Known pre-existing issue (NOT introduced by this pass)
A full 101-page sweep found **19 pages whose content overflows the fixed 210×297mm `.a4-page`
(`overflow:hidden`), so the bottom is clipped on screen/print.** This is pre-existing (the only
page this pass affected here was page 4, now fixed). Confirmed real content loss on page 53
(task 4 is cut). Left untouched to respect the "minimal corrections / no large refactors" scope.
Affected pages (overflow px): 22(47) 27(152) 30(198) 32(16) 36(115) 40(137) 44(143) 46(162)
50(31) 53(337) 58(59) 59(158) 62(110) 63(78) 84(143) 85(40) 87(304) 91(33). Recommend a
separate layout pass.

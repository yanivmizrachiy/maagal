# PROVENANCE — maagal (מעגל)

תיעוד בלבד. הדרישות המחייבות נמצאות ב־`RULES.md`. הנתונים המלאים: `workbook.json` (מקור כל דף ושאלה), `provenance/coverage.json` (מטריצת כיסוי), `provenance/page-accounting.json` (כל דף מהשלב הקודם → דף סופי), `provenance/changes.json` (כל שינוי).

## מקורות

| ריפו | commit | נתיבים | תפקיד |
|---|---|---|---|
| `yanivmizrachiy/smartschool-hebrew-voice-notes` | `760f64e82dc6f309c67324df100399532f89bc8f` | circle/page-1..88.html, styles.css, a4-utilization.css | 88 original circle pages (data-layout c1..c88); byte-identical copies were in razpages |
| `yanivmizrachiy/razpages` | `c8fe7bde7ee19215b5593f9379c3db2f0c846538` | workbooks/circle/ (source/targilim/g8-01,05,06; source/bbb/עמוד-196..205) | Phase-1 import source; targilim cards (data-layout g8-01/05/06); BBB renders (retired, replaced by the official text) |
| `yanivmizrachiy/jerusalem2` | `ffa9833f9f` | public/media/curriculum/idkun-geometri-8/pages/page-003..013.webp, fig-p*.png | copy of the MoE geometry_8.pdf pages used to transcribe and verify the official questions (moe8-*) |
| `yanivmizrachiy/bbb` | `e365c0f3c92d98a379b511aec6aeca032e4a8391` | geometry8/topics/t01_circle.py (+ 57ae2f2 source crops) | curriculum transcription used for coverage; BBB-written A.Q1 kept as supplementary page (bbbsupp-a1) |
| `yanivmizrachiy/smartschool-hebrew-voice-notes (branch chore/world-class-architecture-chatgpt-20260826-2324)` | `d651f7f85248305b7d8e59451e171245e14df311 / 1b771781dc283c83c7b21a598c80e8729b5ff83a / df5abb7` | circle/page-89..91.html; official-wording edits | unique unmerged work: sector page (br-c90), circle symmetry/congruence page (br-c91), 'קו הגבול' wording replaced by the official definition |

תוכנית הלימודים: משרד החינוך, „תחום גאומטרי לכיתה ח” (geometry_8.pdf, עדכון תשפ״ז) — https://meyda.education.gov.il/files/Pop/0files/matmatika/Chativat-Beynayim/curriculum/updating/geometry_8.pdf

## מספרים

- דפים: **103** (101 phase-1 pages − 10 replaced/merged/retired + 12 added = 103 final pages).
- שאלות: **387**, מתוכן **16** בלוקים של שאלות מתוך תוכנית הלימודים (15 שאלות רשמיות).
- שורות כיסוי: Counter({'imported': 31, 'other-repo': 14, 'irrelevant': 2}).
- שינויים מתועדים: 310 ({'other': 34, 'fix-figure': 46, 'fix-table': 33, 'overflow': 31, 'fix-math': 21, 'dedupe-vary': 30, 'fix-wording': 64, 'dedupe-remove': 5, 'internal-text': 11, 'sub-bullets': 6, 'page-ref': 1, 'keep-label': 1, 'official-presentation': 20, 'ported-from-branch': 7}).

## טרנספורמציות מבניות (כל הדפים)

- שלב 1 (העתקה): תוכן זהה בית־לבית למקור; שינויי נתיב בלבד.
- חומר שנטען בזמן ריצה (loader) הפך לדפים סטטיים; החרוט פוצל מקובץ אחד ל־page-N.html (נבדק: זהות פיקסלים/גאומטריה).
- מספרי שאלות הוסרו; תבליט גדול לשאלה, קטן לסעיף; כותרת תוכנית הלימודים לפי RULES §5.
- כללי CSS שהיו קשורים למספר הדף הגלוי הועברו ל־`data-layout` (תיקן 17 דפי מעגל שחרגו מ־A4).
- סדר פדגוגי לפי RULES §6 (שלבים ב־`workbook.json`).

## חשבון דפים (דפי השלב הקודם → סופי)

| דף קודם | layout | דף סופי | סטטוס | סיבה |
|---|---|---|---|---|
| 1 | `c1` | 1 | preserved | same page |
| 2 | `c2` | 2 | preserved | same page |
| 3 | `c3` | 3 | preserved | same page |
| 4 | `c4` | 4 | preserved | same page |
| 5 | `c5` | 5 | preserved | same page |
| 6 | `c6` | 10 | moved | pedagogical order (RULES §6): stage 'המעגל וחלקיו' |
| 7 | `c7` | 11 | moved | pedagogical order (RULES §6): stage 'המעגל וחלקיו' |
| 8 | `c8` | 7 | moved | pedagogical order (RULES §6): stage 'המעגל וחלקיו' |
| 9 | `c9` | 8 | moved | pedagogical order (RULES §6): stage 'המעגל וחלקיו' |
| 10 | `c10` | 13 | moved | pedagogical order (RULES §6): stage 'המעגל וחלקיו' |
| 11 | `c11` | 18 | moved | pedagogical order (RULES §6): stage 'רדיוס וקוטר: חישוב, מדידה, יחידות ובעיות' |
| 12 | `c12` | 19 | moved | pedagogical order (RULES §6): stage 'רדיוס וקוטר: חישוב, מדידה, יחידות ובעיות' |
| 13 | `c13` | 14 | moved | pedagogical order (RULES §6): stage 'רדיוס וקוטר: חישוב, מדידה, יחידות ובעיות' |
| 14 | `c14` | 15 | moved | pedagogical order (RULES §6): stage 'רדיוס וקוטר: חישוב, מדידה, יחידות ובעיות' |
| 15 | `c15` | 16 | moved | pedagogical order (RULES §6): stage 'רדיוס וקוטר: חישוב, מדידה, יחידות ובעיות' |
| 16 | `c16` | 20 | moved | pedagogical order (RULES §6): stage 'רדיוס וקוטר: חישוב, מדידה, יחידות ובעיות' |
| 17 | `c17` | 17 | preserved | same page |
| 18 | `c18` | 23 | moved | pedagogical order (RULES §6): stage 'רדיוס וקוטר: חישוב, מדידה, יחידות ובעיות' |
| 19 | `c19` | 21 | moved | pedagogical order (RULES §6): stage 'רדיוס וקוטר: חישוב, מדידה, יחידות ובעיות' |
| 20 | `c20` | 24 | moved | pedagogical order (RULES §6): stage 'רדיוס וקוטר: חישוב, מדידה, יחידות ובעיות' |
| 21 | `g8-06` | 6 | moved | pedagogical order (RULES §6): stage 'המעגל וחלקיו' |
| 22 | `c21` | 25 | moved | pedagogical order (RULES §6): stage 'המספר π' |
| 23 | `c22` | 26 | moved | pedagogical order (RULES §6): stage 'המספר π' |
| 24 | `c23` | 27 | moved | pedagogical order (RULES §6): stage 'המספר π' |
| 25 | `c24` | 28 | moved | pedagogical order (RULES §6): stage 'המספר π' |
| 26 | `c25` | 29 | moved | pedagogical order (RULES §6): stage 'המספר π' |
| 27 | `c26` | 30 | moved | pedagogical order (RULES §6): stage 'היקף המעגל' |
| 28 | `c27` | 31 | moved | pedagogical order (RULES §6): stage 'היקף המעגל' |
| 29 | `c28` | 33 | moved | pedagogical order (RULES §6): stage 'היקף המעגל' |
| 30 | `c29` | 34 | moved | pedagogical order (RULES §6): stage 'היקף המעגל' |
| 31 | `c30` | 32 | moved | pedagogical order (RULES §6): stage 'היקף המעגל' |
| 32 | `c31` | 35 | moved | pedagogical order (RULES §6): stage 'היקף המעגל' |
| 33 | `c32` | 38 | moved | pedagogical order (RULES §6): stage 'היקף המעגל' |
| 34 | `c33` | 36 | moved | pedagogical order (RULES §6): stage 'היקף המעגל' |
| 35 | `c34` | 39 | moved | pedagogical order (RULES §6): stage 'היקף המעגל' |
| 36 | `c35` | 40 | moved | pedagogical order (RULES §6): stage 'שטח העיגול' |
| 37 | `c36` | 41 | moved | pedagogical order (RULES §6): stage 'שטח העיגול' |
| 38 | `c37` | 42 | moved | pedagogical order (RULES §6): stage 'שטח העיגול' |
| 39 | `c38` | 43 | moved | pedagogical order (RULES §6): stage 'שטח העיגול' |
| 40 | `c39` | 44 | moved | pedagogical order (RULES §6): stage 'שטח העיגול' |
| 41 | `c40` | 45 | moved | pedagogical order (RULES §6): stage 'שטח העיגול' |
| 42 | `g8-05` | 68 | moved | pedagogical order (RULES §6): stage 'זווית מרכזית וחלקי עיגול' |
| 43 | `g8-01` | 47 | moved | pedagogical order (RULES §6): stage 'שטח העיגול' |
| 44 | `c41` | 46 | moved | pedagogical order (RULES §6): stage 'שטח העיגול' |
| 45 | `c42` | 50 | moved | pedagogical order (RULES §6): stage 'שטח העיגול' |
| 46 | `c43` | 51 | moved | pedagogical order (RULES §6): stage 'שטח העיגול' |
| 47 | `c44` | 48 | moved | pedagogical order (RULES §6): stage 'שטח העיגול' |
| 48 | `c45` | 52 | moved | pedagogical order (RULES §6): stage 'שטח העיגול' |
| 49 | `c46` | 53 | moved | pedagogical order (RULES §6): stage 'שטח העיגול' |
| 50 | `c47` | 49 | moved | pedagogical order (RULES §6): stage 'שטח העיגול' |
| 51 | `c48` | 54 | moved | pedagogical order (RULES §6): stage 'שטח העיגול' |
| 52 | `c49` | 57 | moved | pedagogical order (RULES §6): stage 'היקף ושטח: ביטויים, תכנון ושרשראות' |
| 53 | `c50` | 55 | moved | pedagogical order (RULES §6): stage 'היקף ושטח: ביטויים, תכנון ושרשראות' |
| 54 | `c51` | 56 | moved | pedagogical order (RULES §6): stage 'היקף ושטח: ביטויים, תכנון ושרשראות' |
| 55 | `c52` | 59 | moved | pedagogical order (RULES §6): stage 'היקף ושטח: ביטויים, תכנון ושרשראות' |
| 56 | `c53` | 60 | moved | pedagogical order (RULES §6): stage 'היקף ושטח: ביטויים, תכנון ושרשראות' |
| 57 | `c54` | 61 | moved | pedagogical order (RULES §6): stage 'היקף ושטח: ביטויים, תכנון ושרשראות' |
| 58 | `c55` | 58 | preserved | same page |
| 59 | `c56` | 62 | moved | pedagogical order (RULES §6): stage 'היקף ושטח: ביטויים, תכנון ושרשראות' |
| 60 | `c57` | 63 | moved | pedagogical order (RULES §6): stage 'יישומים: השוואה, מחיר ומידול' |
| 61 | `c58` | 64 | moved | pedagogical order (RULES §6): stage 'יישומים: השוואה, מחיר ומידול' |
| 62 | `c59` | 65 | moved | pedagogical order (RULES §6): stage 'יישומים: השוואה, מחיר ומידול' |
| 63 | `c60` | 66 | moved | pedagogical order (RULES §6): stage 'יישומים: השוואה, מחיר ומידול' |
| 64 | `c61` | 73 | moved | pedagogical order (RULES §6): stage 'צורות מורכבות ומשפט פיתגורס' |
| 65 | `c62` | 100 | moved | pedagogical order (RULES §6): stage 'העשרה: ריבוע חסום במעגל' |
| 66 | `c63` | 69 | moved | pedagogical order (RULES §6): stage 'זווית מרכזית וחלקי עיגול' |
| 67 | `c64` | 70 | moved | pedagogical order (RULES §6): stage 'זווית מרכזית וחלקי עיגול' |
| 68 | `c65` | 75 | moved | pedagogical order (RULES §6): stage 'צורות מורכבות ומשפט פיתגורס' |
| 69 | `c66` | 77 | moved | pedagogical order (RULES §6): stage 'צורות מורכבות ומשפט פיתגורס' |
| 70 | `c67` | 78 | moved | pedagogical order (RULES §6): stage 'צורות מורכבות ומשפט פיתגורס' |
| 71 | `c68` | 80 | moved | pedagogical order (RULES §6): stage 'צורות מורכבות ומשפט פיתגורס' |
| 72 | `c69` | 67 | moved | pedagogical order (RULES §6): stage 'יישומים: השוואה, מחיר ומידול' |
| 73 | `c70` | 101 | moved | pedagogical order (RULES §6): stage 'משימות מסכמות' |
| 74 | `bbb196` | 9 (bbbsupp-a1), 96 (moe8-p3-1) | replaced | BBB paraphrase split: A.Q1 (BBB-written around the official activity label) -> supplementary page; A.Q2 -> official wording on the curriculu |
| 75 | `bbb197` | 96 (moe8-p3-1) | merged | BBB A.Q3 -> official wording, on one curriculum page together with A.Q2 |
| 76 | `bbb198` | 37 (moe8-p4-1) | merged | BBB B.Q1 (bicycle) -> official wording, curriculum page for circumference (with hexagon + recovered toy-car track) |
| 77 | `bbb199` | 37 (moe8-p4-1) | merged | BBB B.Q2 (hexagon) -> official wording, same curriculum page as the bicycle |
| 78 | `bbb200` | 79 (moe8-p6-1), 74 (moe8-p6-2) | replaced | BBB B.Q3 stadium -> official wording (with recovered lawn-field item); B.Q4 three squares -> official wording |
| 79 | `bbb201` | 74 (moe8-p6-2), 72 (moe8-p7-1) | replaced | BBB B.Q5a circle in square / B.Q5b yin-yang -> official wording (with recovered earrings sector) |
| 80 | `bbb202` | 76 (moe8-p9-1) | replaced | BBB B.Q6 two circles in rectangle + B.Q7 shapes -> official wording |
| 81 | `bbb203` | 22 (moe8-p10-1) | replaced | BBB B.Q8 London Eye -> official wording and official photo; BBB-added circumference part dropped as duplicate |
| 82 | `bbb204` | 102 (moe8-p11-1) | replaced | BBB fountain park (condensed) -> full official text, first page |
| 83 | `bbb205` | 103 (moe8-p11-2) | replaced | BBB fountain park parts 9-10 (continuation, nearly empty page) -> full official text, second page |
| 84 | `c71` | 81 | moved | pedagogical order (RULES §6): stage 'מעגל במערכת צירים: הרביע הראשון' |
| 85 | `c72` | 82 | moved | pedagogical order (RULES §6): stage 'מעגל במערכת צירים: הרביע הראשון' |
| 86 | `c73` | 83 | moved | pedagogical order (RULES §6): stage 'מעגל במערכת צירים: הרביע הראשון' |
| 87 | `c74` | 84 | moved | pedagogical order (RULES §6): stage 'מעגל במערכת צירים: הרביע הראשון' |
| 88 | `c75` | 85 | moved | pedagogical order (RULES §6): stage 'מעגל במערכת צירים: הרביע הראשון' |
| 89 | `c76` | 86 | moved | pedagogical order (RULES §6): stage 'מעגל במערכת צירים: הרביע הראשון' |
| 90 | `c77` | 87 | moved | pedagogical order (RULES §6): stage 'מעגל במערכת צירים: הרביע הראשון' |
| 91 | `c78` | 88 | moved | pedagogical order (RULES §6): stage 'מעגל במערכת צירים: הרביע הראשון' |
| 92 | `c79` | 89 | moved | pedagogical order (RULES §6): stage 'מעגל במערכת צירים: הרביע הראשון' |
| 93 | `c80` | 90 | moved | pedagogical order (RULES §6): stage 'מעגל במערכת צירים: המישור כולו' |
| 94 | `c81` | 91 | moved | pedagogical order (RULES §6): stage 'מעגל במערכת צירים: המישור כולו' |
| 95 | `c82` | 92 | moved | pedagogical order (RULES §6): stage 'מעגל במערכת צירים: המישור כולו' |
| 96 | `c83` | 93 | moved | pedagogical order (RULES §6): stage 'מעגל במערכת צירים: המישור כולו' |
| 97 | `c84` | 94 | moved | pedagogical order (RULES §6): stage 'מעגל במערכת צירים: המישור כולו' |
| 98 | `c85` | 95 | moved | pedagogical order (RULES §6): stage 'מעגל במערכת צירים: המישור כולו' |
| 99 | `c86` | 97 | moved | pedagogical order (RULES §6): stage 'מעגל במערכת צירים: המישור כולו' |
| 100 | `c87` | 98 | moved | pedagogical order (RULES §6): stage 'מעגל במערכת צירים: המישור כולו' |
| 101 | `c88` | 99 | moved | pedagogical order (RULES §6): stage 'מעגל במערכת צירים: המישור כולו' |

**דפים חדשים:**

- דף 9 `bbbsupp-a1` — חוט, נעץ ועיפרון (`yanivmizrachiy/bbb@e365c0f3c92d98a379b511aec6aeca032e4a8391:geometry8/topics/t01_circle.py#g8.t01.A.Q1`)
- דף 12 `br-c91` — סימטריה וחפיפה של מעגלים (`yanivmizrachiy/smartschool-hebrew-voice-notes@1b771781dc283c83c7b21a598c80e8729b5ff83a:circle/page-91.html`)
- דף 22 `moe8-p10-1` — גלגל ענק: קוטר ומרכז (`yanivmizrachiy/jerusalem2@ffa9833f9f:public/media/curriculum/idkun-geometri-8/pages/page-010.webp`)
- דף 37 `moe8-p4-1` — היקף מעגל (`yanivmizrachiy/jerusalem2@ffa9833f9f:public/media/curriculum/idkun-geometri-8/pages/page-004.webp`)
- דף 71 `br-c90` — גזרה — קשת, שטח ויישום (`yanivmizrachiy/smartschool-hebrew-voice-notes@d651f7f85248305b7d8e59451e171245e14df311:circle/page-90.html`)
- דף 72 `moe8-p7-1` — חלק מעיגול (`yanivmizrachiy/jerusalem2@ffa9833f9f:public/media/curriculum/idkun-geometri-8/pages/page-007.webp`)
- דף 74 `moe8-p6-2` — עיגולים בתוך ריבועים (`yanivmizrachiy/jerusalem2@ffa9833f9f:public/media/curriculum/idkun-geometri-8/pages/page-006.webp`)
- דף 76 `moe8-p9-1` — מלבן ועיגולים (`yanivmizrachiy/jerusalem2@ffa9833f9f:public/media/curriculum/idkun-geometri-8/pages/page-009.webp`)
- דף 79 `moe8-p6-1` — ריבוע או מלבן ושני חצאי עיגול (`yanivmizrachiy/jerusalem2@ffa9833f9f:public/media/curriculum/idkun-geometri-8/pages/page-006.webp`)
- דף 96 `moe8-p3-1` — מעגל במערכת צירים (`yanivmizrachiy/jerusalem2@ffa9833f9f:public/media/curriculum/idkun-geometri-8/pages/page-003.webp`)
- דף 102 `moe8-p11-1` — פארק המזרקה (`yanivmizrachiy/jerusalem2@ffa9833f9f:public/media/curriculum/idkun-geometri-8/pages/page-011.webp`)
- דף 103 `moe8-p11-2` — פארק המזרקה (המשך) (`yanivmizrachiy/jerusalem2@ffa9833f9f:public/media/curriculum/idkun-geometri-8/pages/page-011.webp`)

## פריטים פתוחים

- אין.

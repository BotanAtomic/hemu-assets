# hemû assets

Built 2026-11-16 from the app (0.1.41), the website and the design project.

Start with `stores/` for anything going into the App Store or Google Play, and `logo/` for everything else.

Colours: orange `#F37C20`, ink `#1A1A1A`, white `#FFFFFF`.

## logo/

Each logo has the same sub-folders: `svg` (vector master), `pdf` (vector, for print),
`png` (transparent where the art is transparent; several sizes), `jpg` and `webp` (1024).
JPG cannot be transparent: transparent art sits on white, and the white versions on ink.

- `app-icon-production/` — the real app's square icon (`krd.hemu.app`): white "h" on orange, with its dark and tinted versions.
- `app-icon-staging/` — the test app's icon (`krd.hemu.app.staging`), inverted so the two are never confused: orange "h" on white, with its dark (ink on orange) and tinted versions. Never use it in public material.
  - In both folders, `*-rounded-*.png` are for slides and mock-ups only (stores need the square one), and `as-shipped-in-app/` holds the exact files inside the app.
- `mark/` — the "h" alone on a transparent background: orange, black, white.
- `wordmark/` — "hemû" written out:
  - `on-light` (ink with an orange û) for white or light backgrounds
  - `on-dark-white` (white with an orange û) for dark backgrounds, as on hemu.krd
  - `black`, `all-white`, `orange` in one colour
  - The wordmark is cropped tight, with no margin. Leave clear space around it when placing it.
- `wordmark-with-clear-space/` — the same wordmarks with a margin already around them, transparent or on white, ink and orange.
- `lockup/` — the rounded icon with the wordmark, side by side (`horizontal`) or one above the other (`stacked`), for light and dark backgrounds.
- `app-icon-production/ios-sizes` and `android-sizes` — the icon at each size the platforms ask for.
- `favicon/` — `favicon.ico` (16 to 256), `favicon.svg`, PNGs at 16, 32 and 48, `apple-touch-icon-180.png`, `android-chrome-192/512.png`, `maskable-512.png` and the website's `favicon.png`.

## colours/

`palette.json`, `palette.css` and a swatch sheet (`palette.png`, `palette.svg`) with the brand and app colours.

## stores/

Everything a store submission needs, one folder per store and language
(`en-US`, `ar`, `tr`, `fa`, `ckb` Soranî, `kmr` Kurmancî):

- `app-store/<language>/` — name, subtitle, promotional text, keywords, description, "what's new", and `screenshots-6.9-inch/` (1320 × 2868).
- `google-play/<language>/` — title, short description, full description, `phone-screenshots/` (1080 × 1920) and `feature-graphic-1024x500.png`.
- `app-store/shared/app-icon-1024.png` and `google-play/shared/app-icon-512.png`.
- `shared/` — the support, privacy, terms, marketing and data-deletion links, and the suggested category and age rating.
- `LISTING-NOTES.md` — character counts against each store's limit, which folder goes into which store language, and the lines that still need a native speaker.

The App Store offers Arabic and Turkish but no Persian and no Kurdish; Google Play offers
Arabic, Turkish and Persian but no Kurdish (checked 2026-11-16). The Kurdish sets are for a
Google Play custom store listing by country (for example Soranî as the default for Iraq),
an App Store custom product page, ads and the website. Do not put Kurdish text in the Arabic slot.
All text outside English is a draft until a native speaker has read it.

## store-screenshots/

By language (`english`, `sorani`, `kurmanci`, `arabic`, `turkish`, `farsi`), then by store:
`app-store` is 1320 × 2868 and `google-play` is 1080 × 1920, eight screens each
(Home, Sell, Filters, Offers, Listing, Alerts, Follow, Cities), plus the 1024 × 500
Google Play feature graphic. `MANIFEST.md` has the details and the headlines.
All six sets were re-exported on 2026-11-16 with the current wording: a listing is
«ڕیکلام» in Soranî and "reklam" in Kurmancî.

Neither store has a Kurdish listing language, so the Soranî and Kurmancî sets are for
review, custom store pages, ads and social. The Kurmancî and Farsi headlines are new
drafts and need a native speaker to read them before use.

## app-screens/

The same eight screens without the marketing frame and headline, 1179 × 2556, in the
same six languages. The photos are empty placeholders, to be filled for video.

## website-screens/

The phone screens used on hemu.krd (Home, Listing, Profile) in `english`, `sorani`,
`arabic` and `turkish`, as the original WebP and as PNG. The Soranî ones were made before
the wording change of 2026-11-16 and still show the old word for a listing.

## social/

- `profile-pictures/` — square profile pictures in orange, white and ink.
- `banners/` — headers and covers for X, Facebook, LinkedIn and YouTube, the link-preview size, Instagram post and story, TikTok and WhatsApp, each in orange, ink and light.
- `link-preview-1200x630.jpg` — the image shown when hemu.krd is shared.
- `hero-portrait.webp`, `hero-landscape.webp` — the website's hero pictures.

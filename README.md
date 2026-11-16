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

## marketing/

Ready-made images for ads, social, print and store pages, in the six app languages
(`english`, `sorani`, `kurmanci`, `arabic`, `turkish`, `farsi`). Right-to-left languages are mirrored.
The phone screens come from the store screenshots; the headlines are the same lines as the store
screenshots (`store-screenshots/MANIFEST.md`), so the Kurmancî and Farsi headlines are still drafts that
need a native speaker. Only the English cards carry "Available on Google Play and the App Store"; the other
languages show the wordmark, the icon and hemu.krd without it. There are no tablet screenshots and no store badges.

- `ads/<language>/` — one image per feature screen (01 Home … 08 Cities) in four sizes:
  - `square-1080x1080/` — Meta/Instagram feed, Google App campaigns square.
  - `portrait-1080x1350/` — Instagram and Facebook 4:5 feed.
  - `story-1080x1920/` — Stories, Reels, TikTok, Shorts. Text and phone stay inside the safe area (clear of the top 250 px and bottom 420 px).
  - `landscape-1200x628/` — Google App campaigns landscape, Facebook link, X card.
  - Orange background; `01-home` also comes on ink (`-ink`) and on canvas (`-light`).
- `launch/<language>/<size>/hemu-brand-orange.png` and `hemu-brand-ink.png` — brand cards (icon, wordmark, headline 01, hemu.krd), same four sizes.
- `app-store-header-search/<language>/` — Apple's two newer App Store assets, orange, RGB with no transparency:
  - `header-3840x1646.png` — product page header (21:9). Everything that matters sits in the art safe area, 1646 × 661 at x 1097, y 493: the white wordmark and the headline. Phones fill the sides and are cropped differently per device.
  - `search-results-3840x2560.png` — search results asset (3:2). The headline and the top of the three phones (listing, home, offers chat) sit in the safe area, up to 2168 × 1030 at x 836, y 765.
  - Apple's rules: no website address, no store or other platform names, no prices claims. Nothing of that is on these files. The Arabic App Store slot uses the Soranî files (owner's decision).
- `google-play-developer-page/` — `header-4096x2304.png` (wordmark, English headline, three phones; the content stays in the central 60 % because Google crops it) and `developer-icon-512.png`.
- `qr/` — QR codes for Google Play, the App Store and hemu.krd, as PNG (1024) and SVG, black on white with a quiet zone and high error correction. The `-with-icon` versions have the app icon in the centre. All were decoded with OpenCV and read back the right link.
- `youtube/` — `channel-banner-2560x1440.png` (the text sits in the 1546 × 423 safe area) and a 1280 × 720 video thumbnail per language (`thumbnail-1280x720-<language>.png`).
- `print/` — A5 flyer, 1748 × 2480 px (300 dpi), one per language: headline, three phones, the three QR codes labelled Google Play, App Store and hemu.krd, and the wordmark.

Headlines are set in Unbounded Bold for Latin scripts and in the system Arabic font for Soranî, Arabic and Farsi, as in the store screenshots. The files are PNG; none is large enough to need a JPEG.

# hemû store listing text: notes

Written 2026-11-16. Each field is a plain UTF-8 `.txt` file that ends in one newline. Paste the text without that final newline.

## Character counts
Counts are Python `len()` of the NFC string, without the final newline. Every field is within its limit.

| Field | Limit | en-US | ar | tr | fa | ckb | kmr |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| `app-store/name.txt` | 30 | 28 | 27 | 29 | 29 | 22 | 24 |
| `app-store/subtitle.txt` | 30 | 21 | 18 | 21 | 17 | 20 | 22 |
| `app-store/promotional-text.txt` | 170 | 146 | 106 | 115 | 125 | 130 | 154 |
| `app-store/keywords.txt` | 100 | 96 | 97 | 96 | 96 | 99 | 94 |
| `app-store/description.txt` | 4000 | 1809 | 1583 | 1789 | 1850 | 1968 | 2087 |
| `app-store/whats-new.txt` | 4000 | 271 | 261 | 259 | 269 | 288 | 313 |
| `google-play/title.txt` | 30 | 29 | 26 | 28 | 28 | 22 | 24 |
| `google-play/short-description.txt` | 80 | 77 | 74 | 80 | 75 | 72 | 75 |
| `google-play/full-description.txt` | 4000 | 1809 | 1583 | 1789 | 1850 | 1968 | 2087 |

### Rules the copy follows
- **Keywords:** comma-separated with no spaces after commas. They repeat no word from the name or subtitle and name no competitors.
- **Google Play full description:** the same text as the App Store description.
- **Google Play titles:** no "free", "best" or "#1".

## Which folder goes to which store language

### Sources checked on 2026-11-16
- **Apple:** "App Store localizations", App Store Connect Help, https://developer.apple.com/help/app-store-connect/reference/app-store-localizations. It lists 50 languages. It includes Arabic and Turkish. It has no Persian and no Kurdish. The page shows no last-updated date. Its country table shows:
  - Iraq: default English (U.K.), with Arabic as an additional language.
  - Türkiye: default English (U.K.), with Turkish as an additional language.
- **Google:** "Translate and localize your app", Play Console Help, https://support.google.com/googleplay/android-developer/answer/9844778, under "View list of available languages". It lists:
  - Arabic – ar
  - Turkish – tr-TR
  - Persian – fa, fa-AE, fa-AF, fa-IR
  - English (United States) – en-US

  It lists no Kurdish code (ku, ckb or kmr).

### Mapping

| Folder | App Store Connect | Google Play Console |
| --- | --- | --- |
| `en-US` | English (U.S.) | English (United States) – en-US |
| `ar` | Arabic | Arabic – ar |
| `tr` | Turkish | Turkish – tr-TR |
| `fa` | **Not offered.** No Persian localization. | Persian – fa (or fa-IR) |
| `ckb` (Soranî) | **Not offered.** No Kurdish. | **Not offered.** No Kurdish. |
| `kmr` (Kurmancî) | **Not offered.** No Kurdish. | **Not offered.** No Kurdish. |

### Text for languages a store does not offer
The text is still delivered for these uses:
- `ckb` and `kmr` on both stores;
- `fa` on the App Store.

Use it for:
- **Google Play custom store listings**, targeted by country, for example a Soranî listing for Iraq;
- **App Store custom product pages:** these use the same localizations, so a Kurdish page has to live in a supported locale;
- ads, social posts and the website.

Do not upload Kurdish text into the Arabic slot.

### English (U.K.)
Iraq and Türkiye use English (U.K.) as their default App Store language. Add an English (U.K.) localization with the `en-US` text so those storefronts do not show only the primary language.

### Old screenshot manifest
The screenshot MANIFEST used "Turkish – tr-TR" and "Arabic", which matches. That manifest had no Persian set.

## Facts used and their sources
Every feature in the copy appears in the app strings (`locales/*/common.json`, rel-0124). Feature names use the app's own words.

| Topic | Source |
| --- | --- |
| Listing | ڕیکلام / reklam / إعلان / ilan / آگهی |
| Offer and counter-offer | `chat.v2.makeOffer`, `counterOffer`, `acceptAmount` |
| Saved searches and alerts | `settings.savedSearches`, `search.turnOffAlerts` |
| Favourites | `favorites.title` |
| Follow sellers | `account.guestFollow`, `home.peopleYouFollow` |
| Report and block | `listing.reportListing`, `chat.report`, `settings.blockedUsers` |
| Photo and location in chat | `chat.v2.camera`, `chat.v2.locationTitle` |
| Display currencies | `settings.currency*`, `settings.displayCurrencyDescription` |
| Categories | `categories.*` |
| All Kurdistan / several locations | `location.allKurdistan`, `home.moreLocations` |
| Browse as a guest; sign in to post, message, save and follow | `onboarding.startBrowsing`, the sign-in prompts |
| Delete account | `settings.deleteAccount` |

### Two facts the copy keeps
- **Payments:** "No payment is made in hemû". This comes from `chat.v2.agreementNote`, "No payment is made here."
- **Price:** "Free" / "free to use" only. No "no fees ever".

### Facts from READINESS
- Minimum age 13.
- Banned goods are not allowed.
- Reports are reviewed.
- Support email hello@hemu.krd.

### What the copy leaves out
The copy does not mention:
- AI, ranking claims, user counts, security or encryption, or verified sellers;
- payments, delivery or competitors;
- the 24-hour response target, which is still an open gate.

### Checks run
I grepped the output for these and found none:
- ئیعلان in `ckb`;
- îlan or ilan in `kmr`;
- AI, #1, best, secure, encrypt, verified, safe and "!" in every locale.

The `ckb` text has no Latin or Persian digits outside URLs and the email address. It uses ١٣.

## NEEDS A NATIVE-SPEAKER READ
Have a native speaker read every locale except `en-US` in full before publishing. These are the lines I am least sure about.

### Soranî (`ckb`)
- **Name:** «hemû – بازاڕی کوردستان». Check that «بازاڕ» is the right word for a marketplace app, rather than a physical bazaar.
- «نرخی گۆڕدراو خەمڵاندنە». Check that the wording is natural.
- «فرۆشتنی کاڵای نایاسایی و ڕێگەپێنەدراو ڕێگەی پێ نادرێت». The sentence repeats «ڕێگە».
- **Heading:** «بازاڕێک کە ڕێز لە هەمووان دەگرێت».
- **Arabic loanwords kept on purpose** because the app uses them: «قبوڵ» (accept) and «حەز». Decide whether to swap them for Kurdish words.
- **Keywords:** check that «دەستی دووەم», «شوقە» and «مۆبایل» are the words people actually search for.

### Kurmancî (`kmr`)
- **"xulek" for minute** ("di xulekekê de"). I chose it over the Arabic loanword "deqe", which the website uses ("di deqeyekê de"). Confirm the choice, and also update the website, which still says "îlana te" (must become "reklama te").
- **"bihayên veguherandî texmîn in":** "texmîn" is an Arabic loanword, but the app uses it in `displayCurrencyDescription`.
- **"Destûr nayê dayîn ku tiştên li dijî zagonê an yên ku mercên me rê nadin werin firotin."** Check the grammar and whether it sounds natural.
- **Heading "Bazareke ku rêzê li her kesî digire".**
- **"Gava ku tu biweşînî, kiryar yekser reklama te dibînin".**
- **"Lêgerînê tomar bike; dema reklameke nû ya lê dikeve tê weşandin…"** Check "lê dikeve" for "matches".
- **"hesab"** (account) is an Arabic loanword, kept because the app uses it.
- **Keywords:** check that "destê duyem" is a natural search term.

### Arabic (`ar`)
- **Tip:** «التقيا في مكان عام وافحص الغرض قبل أن تدفع». It mixes the dual and the singular.
- **Keyword:** check that «مبوبة» is natural for the target audience.
- **Digits:** decide whether to use Eastern Arabic digits (١٣) or Western digits for Iraqi readers.

### Turkish (`tr`)
- **Short description:** exactly 80 characters, the limit.
- **"Kürdistan" on the Türkiye storefront:** decide whether "Kürdistan" and the Hewlêr/Amed line should appear there. A wording choice like "Kürdistan'ın her yerinde" may be sensitive there. The app and website use it already.

### Persian (`fa`)
- **Wording:** the description mixes informal "تو" and plural "کنید" like the app does. Confirm the tone.
- **Keyword:** check that «سنندج,کرمانشاه» suit the Iranian audience.
- **Iran:** whether to target Iran at all is the owner's decision, given store availability there.

### All locales
- The language line (in each language's own script) is shown as one line in RTL descriptions. Check how it renders in the store preview.
- "You must be 13 or older" depends on the final Terms. Check it once the Terms are live.

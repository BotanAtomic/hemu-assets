# hemû store screenshots: file manifest

102 PNG files in six languages, re-exported on 2026-11-16. Every file was exported at full size from the design pages in this project.

| Folder | Store | Size | Files |
| --- | --- | --- | --- |
| `<language>/app-store/` | App Store, iPhone 6.9″ | 1320 × 2868 | `01-home` … `08-cities` |
| `<language>/google-play/` | Google Play, phone | 1080 × 1920 | `01-home` … `08-cities` |
| `<language>/google-play/feature-graphic.png` | Google Play feature graphic | 1024 × 500 | 1 |

Screen order is the same in every language: 01 Home, 02 Sell, 03 Filters, 04 Offers, 05 Listing, 06 Alerts, 07 Follow, 08 Cities.

## english/ (17 files)
- **Source page:** Store Screenshots.dc.html
- **Use:** default listing on both stores.

## arabic/ (17 files)
- **Source page:** Store Screenshots.dc.html, Arabic section (text in store-langs.js)
- **Store locale:** App Store "Arabic" and Google Play "Arabic".
- **Layout:** right to left, with Eastern Arabic digits for counts and dates. Prices stay as written.
- **Headlines:** اشترِ وبِع في كل كردستان · بِع خلال دقيقة من كاميرتك · اعثر على ما تريده بالضبط · اتفقا على السعر داخل المحادثة · كل التفاصيل قبل أن تلتقيا · تنبيهات فورية لعمليات بحثك · تابع البائعين الذين تحبهم · مدينتك، أو كل كردستان

## turkish/ (17 files)
- **Source page:** Store Screenshots.dc.html, Turkish section (text in store-langs.js)
- **Store locale:** App Store "Turkish" and Google Play "Turkish – tr-TR".
- **Headlines:** Kürdistan’ın her yerinde al ve sat · Kameranla bir dakikada sat · Aradığını hemen bul · Fiyatta sohbet içinde anlaşın · Buluşmadan önce tüm detaylar · Kayıtlı aramalar için bildirim al · Satıcıları takip et · Şehrin ya da tüm Kürdistan

## farsi/ (17 files)
- **Source page:** Store Screenshots.dc.html, Farsi section (text in store-langs.js)
- **Store locale:** App Store "Persian" and Google Play "Persian".
- **Layout:** right to left, with Persian digits (۰–۹) for counts and dates. Prices stay as written, as in Arabic.
- **Headlines (new drafts):** در سراسر کردستان بخر و بفروش · با دوربینت در یک دقیقه بفروش · همان چیزی را که می‌خواهی دقیقاً پیدا کن · در همان گفتگو روی قیمت توافق کنید · همهٔ جزئیات پیش از دیدار · برای جستجوهای ذخیره‌شده هشدار بگیر · فروشنده‌های مورد علاقه‌ات را دنبال کن · شهر خودت، یا همهٔ کردستان

## sorani/ (17 files): Sorani Kurdish, not a store locale
- **Source page:** Store Screenshots.dc.html, Sorani section (text in store-langs.js)
- **Not for a language slot:** neither store has a Kurdish listing language, so do not upload this set under Arabic.
- **Use:** native-speaker review, then a Google Play custom store listing for Iraq, App Store custom product pages, ads and social.
- **Layout:** right to left, with Eastern Arabic digits for counts and dates. A listing is «ڕیکلام».
- **Headlines:** لە هەموو کوردستان بکڕە و بفرۆشە · بە کامێراکەت زوو بیفرۆشە · ئەوەی دەتەوێت ڕێک بیدۆزەرەوە · لەسەر نرخ لە چاتدا ڕێک بکەون · هەموو وردەکارییەک پێش ئەوەی یەک ببینن · ئاگادارکردنەوە بۆ گەڕانەکانت · شوێن فرۆشیارە دڵخوازەکانت بکەوە · شارەکەت، یان هەموو کوردستان

## kurmanci/ (17 files): Kurmanci Kurdish, not a store locale
- **Source page:** Store Screenshots.dc.html, Kurmanci section (text in store-langs.js)
- **Not for a language slot:** neither store has a Kurdish listing language, so do not upload this set under Turkish.
- **Use:** native-speaker review, then custom store listings, App Store custom product pages, ads and social.
- **Layout:** left to right, Latin digits. A listing is "reklam".
- **Headlines (new drafts):** Li seranserê Kurdistanê bikire û bifiroşe · Bi kameraya xwe di deqeyekê de bifiroşe · Tam tiştê ku dixwazî bibîne · Di axaftinê de li ser bihayê li hev bikin · Hemû hûrgilî berî ku hûn hev bibînin · Ji bo lêgerînên tomarkirî agahdariyan bistîne · Firoşkarên ku hez dikî bişopîne · Bajarê te, an jî hemû Kurdistan

## Before publishing
- **Translations:** a native speaker should review all Arabic, Turkish, Farsi, Sorani and Kurmanci text. The Farsi and Kurmanci headlines are new drafts. App text uses hemu-mobile's `locales/*/common.json` wherever a key exists. Listing titles, chat messages and headlines were written for these screenshots.
- **Font:** Arabic, Farsi and Sorani render in the computer's system Arabic font, because the app ships no font of its own. On an iPhone the app would use SF Arabic, which looks slightly different.
- **Sorani prices:** whether prices use Eastern Arabic digits is still undecided. These files keep prices in Latin digits, as do Arabic and Farsi.
- **Making changes:** edit the language's entry in store-langs.js, then re-export. Layout changes made to the English artboards carry over to all five translated sets.

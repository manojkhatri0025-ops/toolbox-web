# ToolBox Web — sudhareko version

## File

- `toolbox-web/`: sudhareko websiteko pura folder.
- `toolbox-web-fixed.zip`: Cloudflare Pages ma upload garna milne website ZIP.
- `configure-site-url.cjs`: asli hosting URL paayepaxi canonical metadata ra sitemap update garne helper.

Contact email: **manojkhatri0025@gmail.com**.

## Sudhar

- Calculator: `50% = 0.5`, `200 × 10% = 20`; scientific notation, unary minus, malformed input ra result precision sudhareko.
- Text converter: Nepali, accented letters ra combining marks preserve hunxan.
- QR: Nepali/emoji UTF-8 encoding; Wi-Fi password/SSID ka spaces ra special characters preserve hunxan.
- PNG compression: PNG format ra transparency preserve hunxa. Lossless output thulo bhaye original file nai dinxa; size ghataune guarantee xaina. PNGko quality slider disabled hunxa.
- Crop preset: wide/tall image ra drag-resize garda ratio ra boundary maintain hunxan.
- Image/PDF: corrupt filele error dekhauxa; generation atkidaina. Filenames safe textko rupma dekhinxan.
- JSON: thulo number, ID ra original numeric value badlidaina. URL decodele literal `+` preserve garxa.
- Khali ad boxes ra verify nabhayeka social account links hataiyeko. AdSense integration pachhiko charanma garne.

## Janch

52 calculator/BMI assertions ra 47 text/QR assertions pass bhaye. QR testma actual qrcode-generator bata baneko QR actual jsQRle decode gari Nepali/emoji compare gariyo. Native canvasma PNG transparency, crop presets, corrupt-file recovery, real 2-page image PDF ra 3-page merged PDF janchiyo. JSON/URL regression test pani pass bhayo.

## Cloudflare deployment

Website URL: https://toolbox-web-3fv.pages.dev

Project name: `toolbox-web`.

Canonical metadata, robots.txt ra 30-page sitemap asli URL anusar configure bhayeka xan. Cloudflareko extensionless URL anusar canonical ra sitemap milaieko xa.

### Paxi update garne tarika

1. Cloudflare dashboardma Workers & Pages → toolbox-web → Create a new deployment kholne.
2. Production chhanne ra updated `toolbox-web-fixed.zip` upload garne. ZIP bhitra `index.html`, `css`, `js`, `assets` ra `tools` rootma xan.
3. Save and Deploy garda existing public URL ma naya version aauxa.
4. Homepage ra pariwartan gareka tools kholera janchne.

Technical helper: Node.js bhaye outputs directoryma `node configure-site-url.cjs https://YOUR-ACTUAL-HOST` chalayera `toolbox-web` folder feri upload garna milxa. Example hostnameko thau ma Cloudflarele diyeko asli URL nai rakhnu.

Sitemap: https://toolbox-web-3fv.pages.dev/sitemap.xml

Asli address set bhayeko xa. Naya domain jodyo bhane matra configure-site-url.cjs feri chalaune.

[Cloudflare Direct Upload guide](https://developers.cloudflare.com/pages/get-started/direct-upload/) · [Cloudflare Pages limits](https://developers.cloudflare.com/pages/platform/limits/)

## AdSense

Timro existing AdSense accountma yo naya website add garera reviewma pathaune charan pachhi aauxa. Khali account bhayeko bharma naya website automatically approved hudaina. Ahile ads script wa publisher ID jodiyeko xaina.

## Libraries

Websitele pinned CDN libraries use garxa: pdf-lib 1.17.1 (MIT), jsPDF 2.5.1 (MIT), qrcode-generator 1.4.4 (MIT), jsQR 1.4.0 (Apache 2.0). Browserma file processing local hunxa; suruma library load huna internet chahinxa.

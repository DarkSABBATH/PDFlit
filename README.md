# PDFlit

Free document to Markdown converter. Runs entirely in the browser — no uploads, no backend, no accounts.

Supports PDF, Word (.docx), HTML, and plain text. Output as `.md`, `.txt`, or `.html`. Batch convert and download as a zip.

## What it does

- Converts PDF, Word, HTML, and TXT files to clean Markdown
- Everything runs client-side — files never leave the user's device
- Batch upload with per-file status tracking
- Side-by-side Markdown editor and live preview
- Download individual files or everything as a `.zip`
- Conversion history stored in localStorage (last 5 files)
- AdSense-ready ad slots

## Stack

No framework, no build step. Just an `index.html` file.

- [PDF.js](https://mozilla.github.io/pdf.js/) — PDF parsing
- [Mammoth.js](https://github.com/mwilliamson/mammoth.js) — Word (.docx) to HTML
- [Turndown](https://github.com/mixmark-io/turndown) — HTML to Markdown
- [Marked](https://marked.js.org/) — Markdown rendering
- [JSZip](https://stuk.github.io/jszip/) — zip download

All loaded from cdnjs, no npm required.

## Deploy

### Vercel (recommended)

1. Fork or clone this repo
2. Go to [vercel.com](https://vercel.com) and import the repo
3. Leave all settings as default and hit Deploy

That's it. You'll get a live URL like `pdflit.vercel.app`.

### Netlify

Same deal — drag the folder into [app.netlify.com/drop](https://app.netlify.com/drop) and it's live instantly.

### Custom domain

Once deployed, add your domain in the Vercel/Netlify dashboard. DNS propagation usually takes under an hour.

## Ads

Three AdSense placeholder slots are already in the HTML:

- `ad-leaderboard` — below the hero (728×90)
- `ad-mid` — between the converter and history (728×90)

Replace the comments inside those divs with your AdSense snippet when your account gets approved.

## Local development

No build step needed. Just open `index.html` in a browser.

```bash
git clone https://github.com/yourusername/pdflit
cd pdflit
open index.html
```

Or use a local server to avoid browser file:// restrictions:

```bash
npx serve .
```

## License

MIT

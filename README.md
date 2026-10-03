# NSE/BSE Positive News Alerts

A free, static web page that monitors public Indian market RSS feeds and shows **positive** stock-related news with direct links.

## Features

- Pulls headlines from Economic Times Markets, LiveMint Markets, and Business Standard Markets
- Simple keyword filter for positive news (surge, rally, profit, beats estimates, record high, etc.)
- Browser notifications for new positive items
- Auto-refresh every 3 / 5 / 10 minutes (or off)
- Remembers already-seen news (localStorage)
- Fully free — no API keys, no backend, no paid services
- Works offline after first load (cached in browser)

## Deploy on GitHub Pages (free)

1. Create a new public repository on GitHub (e.g. `nse-bse-news-alerts`).
2. Upload (or push) the `index.html` file to the **root** of the repository.
3. Go to **Settings → Pages**.
4. Under **Source**, choose **Deploy from a branch**.
5. Select branch `main` (or `master`) and folder `/ (root)`.
6. Click **Save**.
7. Wait 1–2 minutes. Your site will be live at:
   `https://YOUR-USERNAME.github.io/nse-bse-news-alerts/`

Optional: add a custom domain later under the same Pages settings.

## How the positive filter works

A headline is considered positive if it contains at least one positive keyword **and** none of the negative keywords.

You can edit the `POSITIVE` and `NEGATIVE` arrays in `index.html` to tune the filter.

## Limitations (honest)

- Keyword-based only — not real ML sentiment. Occasional false positives/negatives are possible.
- Depends on the free public `rss2json.com` service (rate limits apply if many people hit it hard).
- RSS feeds update a few times per hour; this is not a high-frequency trading alert.
- Not financial advice. Always read the full article and do your own research.

## Local testing

Just open `index.html` in any modern browser, or serve it with any static server:

```bash
npx serve .
# or
python -m http.server 8000
```

## License

MIT — free to use, modify, and share.

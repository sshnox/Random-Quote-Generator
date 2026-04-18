# The Daily Quotation

A random quote generator with an editorial, newspaper-inspired design. Pulls quotes from the [Quotable](https://github.com/lukePeavey/quotable) public API (with a ZenQuotes fallback and a built-in local library) and displays them with a gentle fade animation. Includes copy-to-clipboard and a post-to-X button.

## Features

- Random quotes from a public API, with two live fallbacks and a 30-quote offline library so it never breaks
- Smooth cross-fade animation when a new quote loads
- Copy-to-clipboard button (uses the modern Clipboard API, falls back to `execCommand` on older browsers)
- "Post to X" share button (pre-fills tweet text)
- Keyboard shortcuts: `Space` / `N` for a new quote, `C` to copy
- Zero build step, zero dependencies. One HTML file.
- Fully responsive, with `prefers-reduced-motion` support

## Run locally

Just open `index.html` in a browser. That's it.

```bash
# Or, if you prefer a local server:
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

**Option A — Drag-and-drop (easiest):**

1. Create a new repo on GitHub.
2. Upload `index.html` (and this README) to the root of the repo.
3. In the repo, go to **Settings → Pages**.
4. Under **Source**, select **Deploy from a branch**, pick `main` and `/ (root)`, then save.
5. Your site will be live at `https://<your-username>.github.io/<repo-name>/` within a minute.

**Option B — Git CLI:**

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

Then enable Pages under **Settings → Pages** as above.

**Option C — Automatic deploy via GitHub Actions:**

This repo includes a workflow at `.github/workflows/deploy.yml` that automatically publishes the site to GitHub Pages on every push to `main`. To use it:

1. Push this repo to GitHub.
2. Go to **Settings → Pages** and set **Source** to **GitHub Actions**.
3. Push any commit — the site deploys automatically.

## File structure

```
.
├── index.html              # The entire app (HTML + CSS + JS)
├── README.md
└── .github/
    └── workflows/
        └── deploy.yml      # Optional: auto-deploy to GitHub Pages
```

## Credits

- Typography: Playfair Display, Cormorant Garamond, DM Mono (Google Fonts)
- Quote API: [Quotable](https://github.com/lukePeavey/quotable) (primary), [ZenQuotes](https://zenquotes.io/) (fallback)

## License

MIT — do whatever you like with it.

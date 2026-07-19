# fructus-web

Marketing site for [Fructus](https://github.com/solutionbyhour) — a self-hosted AI portfolio analyst.

Single-page, hand-written HTML with Tailwind via CDN. No build step. Deployed via GitHub Pages from the `main` branch.

## Local preview

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

## Deploy

Any push to `main` triggers a GitHub Pages rebuild.

## Structure

- `index.html` — the whole page
- `images/` — PDF page screenshots used in the "Sample output" section

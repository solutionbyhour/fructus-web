# fructus-web

Explainer page for [Fructus](https://solutionbyhour.github.io/fructus-web/), a self-hosted portfolio server I built for myself. This isn't a landing page for a product you can buy. It's the thing I link to when I want to answer the question "what did you build?" in one URL instead of ten paragraphs.

Live at **https://solutionbyhour.github.io/fructus-web/**.

## What lives here

- `index.html`, the whole page. Everything is inline: markup, Tailwind classes (via CDN), one small block of custom CSS at the top of the `<head>`.
- `images/`, three PNGs pulled from the actual Fructus PDF output. Used in the "sample output" section so visitors see the real thing instead of stock illustrations.
- `.nojekyll`, so GitHub Pages skips its Jekyll pipeline and serves the file tree as-is.

That's it. No build step, no `package.json`, no framework.

## Editing

Open `index.html` in whatever editor you like. Change copy, adjust colors in the `tailwind.config` block near the top, or drop in a new screenshot under `images/` and reference it in the "Sample output" section.

To preview locally:

```bash
python3 -m http.server 8080
# then open http://localhost:8080
```

The Tailwind CDN handles the styling live, so what you see locally is what ships.

## Publishing

Push to `main`. GitHub Pages picks it up within a minute or two. To watch the build:

```bash
gh api repos/solutionbyhour/fructus-web/pages --jq '{status, html_url}'
```

## When to touch this

- The Fructus codebase gained a real new feature. Add a card to the features grid, or a paragraph to the "what it does" section.
- I generated a fresh set of PDF outputs and the screenshots feel stale. Regenerate the pages with `pdftoppm -png -r 130` from the real PDFs and replace the three files in `images/`.
- The Medium article got published or updated. Consider adding a soft link near the top so visitors coming in cold have a way to read the long-form story.

## What this is not

- Not a product page. There is no signup, no pricing, no "join the waitlist."
- Not a marketing site. It doesn't try to sell Fructus to anyone.
- Not an interactive demo. Fructus needs a brokerage connection and a personal Gemini key. Neither can be safely wired into a public web page.

It is a static explainer. That is the entire scope.

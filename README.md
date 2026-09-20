# agentic9.ai

Static marketing and documentation site for **Agentic9 Crew**, served at
[agentic9.ai](https://agentic9.ai) via GitHub Pages. Plain HTML and CSS,
no build step, no Jekyll (`.nojekyll` is present).

## Files

- `index.html` – landing page
- `docs/index.html` – architecture overview
- `styles.css` – shared stylesheet (dark by default, light via `prefers-color-scheme`)
- `favicon.svg`, `robots.txt`, `CNAME`, `.nojekyll`

## Deploy

1. Push to the repository's default branch.
2. In the repository settings, under **Pages**, set the source to *Deploy from a
   branch*, choose the default branch and the `/ (root)` folder.
3. Set the custom domain to `agentic9.ai` (the `CNAME` file must stay as is) and
   enable *Enforce HTTPS*.

DNS for `agentic9.ai` should point at GitHub Pages (A/AAAA records for the apex,
or a CNAME for `www`), as described in the GitHub Pages documentation.

## Local preview

    python3 -m http.server 8000

then open <http://localhost:8000>.

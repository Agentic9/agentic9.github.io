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

Deployed by GitHub Actions (`.github/workflows/deploy.yml`) as a Cloudflare Worker serving static assets on `agentic9.ai`. Repository secrets: `CLOUDFLARE_API_TOKEN`, `CLOUDFLARE_ACCOUNT_ID`. The `CNAME` and `.nojekyll` files are left for the GitHub Pages fallback until DNS is switched; disable Pages once the Worker serves the domain.

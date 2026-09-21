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

A Cloudflare Worker serving static assets on `agentic9.ai`. Deploy from a machine logged in to Cloudflare with `npx wrangler deploy` (or `infra/deploy.sh --site` in the `agentic9` repo). `.github/workflows/deploy.yml` is a manual fallback that needs `CLOUDFLARE_API_TOKEN` and `CLOUDFLARE_ACCOUNT_ID` as repository secrets. The `CNAME` and `.nojekyll` files are left for the GitHub Pages fallback until DNS is switched; disable Pages once the Worker serves the domain.

# graphclaw.ai

Public landing site and documentation index for **GraphClaw** — open-source
graph-based AI task orchestration. A lite, static, JS-free site served from GitHub
Pages. Sister project of [The Agents and Actions](https://theagentsandactions.com).

## Structure

- `index.html` — marketing landing page (hero, features, how-it-works, explainability
  visuals, architecture/tech stack, self-host CTA). Brand-aligned to the cockpit's
  sky-blue palette and Inter typography.
- `docs/index.html` — curated docs hub linking backend and cockpit documentation.
- `logo.svg` — brand mark (graph-node motif, sky-blue) used for the header and favicon.
- `favicon.svg` — favicon (same mark).
- `social-card.svg` — Open Graph / Twitter card source (1200×630, sky-blue).
- `robots.txt` — crawler policy.
- `sitemap.xml` — discoverability map.
- `CNAME` — custom domain mapping for GitHub Pages.

Both pages cross-reference the parent site, `theagentsandactions.com`, in a top bar and
footer so the relationship is clear when GraphClaw is embedded as a tab there.

## Design notes

- **Lite & static:** no build step, no framework, no JS runtime — inline CSS only.
- **Mobile-first:** single-column by default; grids expand at `min-width` breakpoints.
  Touch targets are ≥44px and the layout has no horizontal scroll down to 320px.
- **Theming:** brand tokens in `:root`, with a `prefers-color-scheme: dark` variant.
- **Assets:** SVG only — the 4.6 MB raster `logo.png` from the cockpit is intentionally
  not shipped here.

### Follow-up (optional)

OG/Twitter previews render most reliably as raster. `social-card.svg` is the source; if
needed, export a `social-card.png` (1200×630) and point `og:image`/`twitter:image` at
it. Real cockpit screenshots could replace the inline illustrations later (requires
running the full Docker stack).

## Publish model

GitHub Pages serves the static content from the `main` branch (see
`.github/workflows/pages.yml`).

## Local preview

Use any static file server from the repo root, for example:

```bash
python -m http.server 4173
```

Then open `http://localhost:4173`.

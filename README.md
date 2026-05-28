# graphclaw.ai

Public landing site and documentation index for GraphClaw.

## Structure

- `index.html` - landing page
- `docs/index.html` - curated docs hub linking backend and cockpit documentation
- `robots.txt` - crawler policy
- `sitemap.xml` - discoverability map
- `CNAME` - custom domain mapping for GitHub Pages

## Publish Model

GitHub Pages serves the static content from the `main` branch.

## Local Preview

Use any static file server from repo root, for example:

```bash
python -m http.server 4173
```

Then open `http://localhost:4173`.
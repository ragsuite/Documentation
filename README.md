# RAGSuite Docs (Mintlify)

Official RAGSuite product documentation.

**Live docs:** [docs.ragsuite.de](https://docs.ragsuite.de)  
**Product:** [www.ragsuite.de](https://www.ragsuite.de)  
**Source code:** [github.com/ragsuite/RAGSuite](https://github.com/ragsuite/RAGSuite)  
**Docs repo:** [github.com/ragsuite/Documentation](https://github.com/ragsuite/Documentation)

## Stack

- **Mintlify** (`docs.json` + Markdown)
- **Node 22 LTS** recommended for local preview (`mint dev`)
- Custom assets: `custom.css`, `_static/`

## Local preview

```bash
npm i -g mint@latest
# Prefer Node 22 (newer majors can break Mintlify)
mint dev
```

## Important paths

| Path | Purpose |
|------|---------|
| `docs.json` | Navigation, theme, navbar, footer |
| `GettingStarted/` | Install, CLI, Docker, configuration |
| `Console/` | AI Search, AI Chatbot, projects, auth |
| `SourcesAndConnectors/` | Crawl, documents, MCP, widgets |
| `Enterprise/` | EE features (license required) |
| `_static/` | Logos and favicon |
| `custom.css` | Chrome polish (sidebar, logo label, readability) |
| `.cursor/skills/mintlify-ragsuite-docs/` | Authoring skill for this repo |

## Chrome / custom.css

Keep these rules when editing docs chrome:

- **Logo:** `docs.json` points at mark-only SVGs (`_static/ragsuite-mark-light.svg` / `ragsuite-mark-dark.svg`). The **RAGSuite Docs** title is a CSS `::after` on the home logo link — do not put wordmark text inside the SVG.
- **Never** style all `header a svg` / `header a img`. That stretches Lucide navbar icons into distorted blobs. Size only `header a[href="/"] img` (and footer equivalent); keep Website/GitHub icons at `1rem` square.
- **npm CLI:** No Lucide `package` icon (the cube reads like Cursor’s mark). Text-only link in `docs.json`.
- **Eyebrows:** `"section"` — avoid breadcrumbs that repeat **RAGSuite Docs** above the page H1.
- **Scrollbars:** Hide Mintlify Base UI custom thumbs (they leave a white box in dark mode). Show a **neutral gray** native sidebar scrollbar only — never brand green (`#8fd4ae` / primary).

## Authenticity

Documentation claims follow [ragsuite.de](https://www.ragsuite.de) and the Community Edition repository. Community vs Enterprise differences are labeled. Beta items (n8n, mobile) are stated explicitly.

Published site: [docs.ragsuite.de](https://docs.ragsuite.de).

## License

Documentation © NITSAN / RAGSuite. Community Edition software is Apache License 2.0 — see the product [NOTICE](https://github.com/ragsuite/RAGSuite/blob/main/NOTICE).

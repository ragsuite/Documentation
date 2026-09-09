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
| `.cursor/skills/mintlify-ragsuite-docs/` | Authoring skill for this repo |

## Authenticity

Documentation claims follow [ragsuite.de](https://www.ragsuite.de) and the Community Edition repository. Community vs Enterprise differences are labeled. Beta items (n8n, mobile) are stated explicitly.

Published site: [docs.ragsuite.de](https://docs.ragsuite.de).

## License

Documentation © NITSAN / RAGSuite. Community Edition software is Apache License 2.0 — see the product [NOTICE](https://github.com/ragsuite/RAGSuite/blob/main/NOTICE).

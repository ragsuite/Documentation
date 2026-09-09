---
name: mintlify-ragsuite-docs
description: >-
  Author and maintain RAGSuite Mintlify documentation in the Documentation
  repo. Use when writing or editing docs.json, Index.md pages, Mintlify
  navigation, CE/EE feature copy, install/CLI/Docker guides, or when the user
  mentions Mintlify, ragsuite docs, or documentation for RAGSuite.
---

# RAGSuite Mintlify Docs

## Scope

Work only in the docs repo (`RAGSuite_DOC` / `ragsuite/Documentation`).
Do not modify CE/EE application repos unless the user explicitly asks.

## File conventions

- Config: root `docs.json` (theme, colors, navbar, `navigation.groups`, footer).
- Pages: PascalCase folders; every section page is `…/Index.md`.
- Slugs in `docs.json` omit `.md` (e.g. `GettingStarted/QuickStart/Index`).
- Required frontmatter: `title`, `description`, `sidebarTitle`.
- Prefer Mintlify components: `Card` / `CardGroup`, `Steps`, `Tabs`, `Tip`, `Warning`, `Info`.
- Visual system: [`custom.css`](../../custom.css) (`.rg-*` classes) for light/dark readability.
- Live site: https://docs.ragsuite.de

## Product naming

- **AI Search** and **AI Chatbot** (never “AI Assistant”).
- Paths: `Console/AISearch/`, `Console/AIChatbot/`.
- CLI: **`@ragsuite/ragsuite`** → binary **`ragsuite`**. No other package name.

## CLI truth

All install commands must match:

- https://www.npmjs.com/package/@ragsuite/ragsuite
- `/Users/arun/RAGSUITE/cli/README.md`

Canonical Community install:

```bash
npm install -g @ragsuite/ragsuite@latest
ragsuite init
ragsuite start
```

Ports: API **9090**, Web **9191**, Postgres **5436**, Redis **6382**, Chroma **8004** (native).

## Authenticity rules

1. Prefer ragsuite.de + CE README / CLI README. Do not leak GAPS.md into customer docs.
2. Label **Community** vs **Enterprise**. Mark **Beta** only for n8n and mobile.
3. SSO = Google OIDC. Do not document SAML/generic OIDC.
4. Org RBAC shipped. Admin UI = **Expo**; API = **FastAPI**.

## Writing tone

- Strong, professional, clear to non-experts.
- Short paragraphs; direct imperatives for procedures.
- No fluff; no “AI Assistant”; no Partial SSO/RBAC language.

## Local preview

```bash
nvm use 22   # Mintlify rejects Node 25+
npm i -g mint@latest
mint dev
```

## Checklist

- [ ] `docs.json` slugs resolve
- [ ] Commands match `@ragsuite/ragsuite` README
- [ ] Light/dark CSS still readable
- [ ] No commit/push unless asked

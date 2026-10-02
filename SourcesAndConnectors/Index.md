---
title: "Sources overview"
description: "Bring knowledge into RAGSuite — domain crawl, sitemap XML, documents, text, Q&A pairs — then connect AI apps with MCP and publish widgets."
sidebarTitle: "Sources overview"
icon: "database"
---

<div className="rg-landing-hero">
  <p className="rg-landing-eyebrow">Knowledge in</p>
  <p className="rg-landing-subtitle">
    Bring in the material your team already relies on, connect AI apps, and
    publish AI Search and AI Chatbot where people work.
  </p>
</div>

Answers are only as good as the sources behind them. This section covers how content enters RAGSuite and how you publish search and chat into websites, intranet, or apps.

**Flow**

1. **Ingest** — in the console **Sources** screen, add content to the active project:
   - **Domain** — crawl a website, from a single page up to 5 link levels.
   - **Sitemap XML** — train every page listed in a `sitemap.xml`.
   - **Document** — upload PDF, Word, PowerPoint, Excel, TXT, Markdown, or HTML files.
   - **Text** — write or paste facts, policies, or opening hours.
   - **Q&A Pairs** — teach exact answers to specific questions.
2. **Connect AI apps** — issue keys under Management → [MCP](/SourcesAndConnectors/MCP/Index) so Cursor, Claude, VS Code, and similar hosts can use your projects.
3. **Automate** — the console **Integrations** screen offers API keys and [n8n](/SourcesAndConnectors/N8n/Index) (**Beta**).
4. **Publish** — embed citation-backed AI Search and AI Chatbot widgets where people already work.

Everything stays on your infrastructure. Start with a domain, sitemap, or documents, then add text, Q&A pairs, MCP, and widgets when you are ready.

<div className="rg-cta-panel">
  <p>Ingest content and publish citation-backed widgets where your team works.</p>
  <div className="rg-cta-actions">
    <a className="rg-cta-primary" href="/SourcesAndConnectors/Crawl/Index">Crawl</a>
    <a className="rg-cta-secondary" href="/SourcesAndConnectors/Widgets/Index">Widgets</a>
  </div>
</div>

## In this section

<CardGroup cols={2}>
  <Card title="Crawl" icon="globe" href="/SourcesAndConnectors/Crawl/Index">
    Domain crawl (up to 5 link levels) and sitemap XML sources.
  </Card>
  <Card title="Documents" icon="file-up" href="/SourcesAndConnectors/Documents/Index">
    Upload PDF, Office, text, Markdown, and HTML files.
  </Card>
  <Card title="Text & Q&A pairs" icon="messages-square" href="/SourcesAndConnectors/TextAndQA/Index">
    Written text and exact question–answer pairs.
  </Card>
  <Card title="MCP" icon="plug" href="/SourcesAndConnectors/MCP/Index">
    Keys and setup so AI apps connect to RAGSuite.
  </Card>
  <Card title="n8n (Beta)" icon="git-branch" href="/SourcesAndConnectors/N8n/Index">
    Workflow automation from the Integrations screen — marked Beta.
  </Card>
  <Card title="Widgets & embeds" icon="code" href="/SourcesAndConnectors/Widgets/Index">
    Embed AI Search and AI Chatbot in your apps.
  </Card>
</CardGroup>

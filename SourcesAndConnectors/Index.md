---
title: "Sources overview"
description: "Ingest and connect knowledge — crawl, upload, connectors, MCP, n8n Beta, and widgets."
sidebarTitle: "Sources overview"
icon: "database"
---

<div className="rg-landing-hero">
  <p className="rg-landing-eyebrow">Knowledge in</p>
  <p className="rg-landing-subtitle">
    Bring in the material your team already relies on, connect live sources, and
    publish AI Search and AI Chatbot where people work.
  </p>
</div>

Answers are only as good as the sources behind them. This section covers how content enters RAGSuite and how you publish search and chat into websites, intranet, or apps.

**Flow**

1. **Ingest** — crawl sites (depth 1–5) or upload PDF, DOCX, and TXT.
2. **Connect inbound** — Gmail, Google Drive, Slack, Microsoft Teams, and related [Connectors](/SourcesAndConnectors/Connectors/Index); **n8n** is **Beta**.
3. **Connect outbound MCP** — issue keys under Management → [MCP](/SourcesAndConnectors/MCP/Index) so Cursor, Claude, VS Code, and similar hosts can use your projects.
4. **Publish** — embed citation-backed AI Search and AI Chatbot widgets where people already work.

Everything stays on your infrastructure. Start with crawl or documents, then wire connectors, MCP, and widgets when you are ready.

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
    Pull website content into your corpus (depth 1–5).
  </Card>
  <Card title="Documents" icon="file-up" href="/SourcesAndConnectors/Documents/Index">
    Upload PDF, DOCX, and TXT for indexing.
  </Card>
  <Card title="Connectors" icon="unplug" href="/SourcesAndConnectors/Connectors/Index">
    Inbound Gmail, Drive, Slack, Teams, and marketplace.
  </Card>
  <Card title="MCP" icon="plug" href="/SourcesAndConnectors/MCP/Index">
    Keys and setup so AI apps connect to RAGSuite.
  </Card>
  <Card title="n8n (Beta)" icon="git-branch" href="/SourcesAndConnectors/N8n/Index">
    Workflow automation bridge — marked Beta.
  </Card>
  <Card title="Widgets & embeds" icon="code" href="/SourcesAndConnectors/Widgets/Index">
    Embed AI Search and AI Chatbot in your apps.
  </Card>
</CardGroup>

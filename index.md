---
description: "Official documentation for RAGSuite — self-hosted, citation-backed AI Search and AI Chatbot on your infrastructure."
sidebarTitle: "Home"
keywords:
  - "RAGSuite"
  - "self-hosted RAG"
  - "enterprise AI"
  - "documentation"
---

<div className="rg-landing-hero">
  <p className="rg-landing-eyebrow">docs.ragsuite.de</p>
</div>

<div className="rg-cta-panel">
  <p>
    Install the official Platform Manager CLI from npm, initialize once, and start the stack.
    Console on port <strong>9191</strong>, API on <strong>9090</strong>.
  </p>
  <div className="rg-cta-actions">
    <a className="rg-cta-primary" href="/GettingStarted/QuickStart/Index">Get Started</a>
    <a className="rg-cta-secondary" href="/GettingStarted/InstallCLI/Index">CLI reference</a>
    <a className="rg-cta-secondary" href="https://www.npmjs.com/package/@ragsuite/ragsuite">npm package</a>
  </div>
</div>

```bash
npm install -g @ragsuite/ragsuite@latest
ragsuite init
ragsuite start
```

<section className="rg-landing-section">
  <p className="rg-landing-eyebrow">Product</p>
  <h2 className="rg-landing-section-title">Build on your own sources</h2>
</section>

<CardGroup cols={2}>
  <Card title="AI Search" icon="search" href="/Console/AISearch/Index">
    Citation-backed search across documents and connected sources.
  </Card>
  <Card title="AI Chatbot" icon="message-circle" href="/Console/AIChatbot/Index">
    Streaming chat grounded in your content — every reply cites its source.
  </Card>
  <Card title="Sources & Connectors" icon="plug" href="/SourcesAndConnectors/Index">
    Crawl, upload, Gmail, MCP, and n8n (Beta). Embed where your team works.
  </Card>
  <Card title="Models" icon="brain" href="/Models/Index">
    OpenAI, Anthropic, Mistral, Gemini, or local Custom LLM / Ollama.
  </Card>
</CardGroup>

<section className="rg-landing-section">
  <p className="rg-landing-eyebrow">Open core</p>
  <h2 className="rg-landing-section-title">Community free. Enterprise when you govern.</h2>
</section>

<CardGroup cols={3}>
  <Card title="Community Edition" icon="box" href="/GettingStarted/CommunityVsEnterprise/Index">
    Apache 2.0 — full pipeline, connectors, models, REST API, unlimited users and projects.
  </Card>
  <Card title="Enterprise" icon="building-2" href="/Enterprise/Index">
    SSO, org RBAC, Compare Models, audit, analytics, voice, and mobile (Beta).
  </Card>
  <Card title="Security & Trust" icon="shield" href="/SecurityAndTrust/Index">
    Self-hosted, no telemetry, inspectable source, citations you can verify.
  </Card>
</CardGroup>

<section className="rg-landing-section">
  <p className="rg-landing-eyebrow">Resources</p>
  <h2 className="rg-landing-section-title">Official links</h2>
</section>

<CardGroup cols={3}>
  <Card title="Website" icon="globe" href="https://www.ragsuite.de">
    Product, pricing, and trust center.
  </Card>
  <Card title="GitHub" icon="github" href="https://github.com/ragsuite/RAGSuite">
    Community Edition source (Apache 2.0).
  </Card>
  <Card title="Support" icon="life-buoy" href="/Support/Index">
    sales@ragsuite.de and German service partners.
  </Card>
</CardGroup>

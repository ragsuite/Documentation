---
title: "Platform overview"
description: "RAGSuite platform spine — architecture, REST API, API keys and webhooks."
sidebarTitle: "Platform overview"
icon: "layers"
---

<div className="rg-landing-hero">
  <p className="rg-landing-eyebrow">Open, inspectable stack</p>
  <p className="rg-landing-subtitle">
    FastAPI API, Expo admin console, PostgreSQL, Redis, and ChromaDB — deployable
    natively or with Docker on infrastructure you control.
  </p>
</div>

This section is for engineers who need to integrate, audit, or operate the platform beyond the console UI. The Community Edition source is public under Apache 2.0 so you can read what you run.

**What you will find**

- How services fit together (API, console, databases, vector store).
- The REST surface for automation and embeds.
- API keys and webhooks for event-driven workflows.

Start with architecture if you are deploying; jump to REST API if you are wiring a client.

<div className="rg-cta-panel">
  <p>Inspect the stack, REST API, and integration primitives.</p>
  <div className="rg-cta-actions">
    <a className="rg-cta-primary" href="/Platform/Architecture/Index">Architecture</a>
    <a className="rg-cta-secondary" href="/Platform/RESTAPI/Index">REST API</a>
  </div>
</div>

## In this section

<CardGroup cols={2}>
  <Card title="Architecture" icon="sitemap" href="/Platform/Architecture/Index">
    Services, data stores, and deploy shapes.
  </Card>
  <Card title="REST API" icon="braces" href="/Platform/RESTAPI/Index">
    HTTP API for search, chat, and admin automation.
  </Card>
  <Card title="API keys & webhooks" icon="link-2" href="/Platform/APIKeysAndWebhooks/Index">
    Authenticate clients and subscribe to events.
  </Card>
</CardGroup>

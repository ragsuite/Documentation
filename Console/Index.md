---
title: "Console overview"
description: "Operate AI Search, AI Chatbot, projects, and authentication in the RAGSuite console."
sidebarTitle: "Console overview"
icon: "layout-panel-left"
---

<div className="rg-landing-hero">
  <p className="rg-landing-eyebrow">Console · port 9191</p>
  <p className="rg-landing-subtitle">
    Search, chatbot, sources, and feedback — from a single admin console on your
    infrastructure (Expo UI by default).
  </p>
</div>

After install, day-to-day work happens in the console. Non-technical operators use it to ask questions, check citations, and improve answer quality. Admins use it to manage projects and sign-in.

**What you can do here**

- Run **AI Search** across your corpus and open the source behind every hit.
- Chat with **AI Chatbot** and follow citations on each reply.
- Capture feedback so quality improves over time.
- Isolate knowledge bases with projects; use password auth and 2FA (SSO is Enterprise).

Open `http://localhost:9191` on a local install (or your published console URL).

<div className="rg-cta-panel">
  <p>Explore console workflows for AI Search and AI Chatbot.</p>
  <div className="rg-cta-actions">
    <a className="rg-cta-primary" href="/Console/AISearch/Index">AI Search</a>
    <a className="rg-cta-secondary" href="/Console/AIChatbot/Index">AI Chatbot</a>
  </div>
</div>

## In this section

<CardGroup cols={2}>
  <Card title="AI Search" icon="search" href="/Console/AISearch/Index">
    Citation-backed search across your corpus.
  </Card>
  <Card title="AI Chatbot" icon="message-circle" href="/Console/AIChatbot/Index">
    Streaming chat with a citation on every reply.
  </Card>
  <Card title="Citations & feedback" icon="message-square" href="/Console/CitationsAndFeedback/Index">
    Verify sources and improve answer quality.
  </Card>
  <Card title="Projects" icon="folder" href="/Console/Projects/Index">
    Isolate knowledge bases and configurations.
  </Card>
  <Card title="Authentication" icon="lock" href="/Console/Authentication/Index">
    Password auth and 2FA; SSO is Enterprise.
  </Card>
</CardGroup>

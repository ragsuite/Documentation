---
title: "Introduction"
description: "Install RAGSuite Community Edition with the official CLI, Docker, or a git clone."
sidebarTitle: "Introduction"
icon: "book-open"
---

<div className="rg-landing-hero">
  <p className="rg-landing-eyebrow">Community Edition</p>
  <p className="rg-landing-subtitle">
    Install on your own infrastructure in minutes. Community Edition is Apache 2.0
    and needs no offline license key.
  </p>
</div>

RAGSuite is a self-hosted platform for **AI Search** and **AI Chatbot** — citation-backed answers over your own documents and apps. Nothing phones home: you run the stack on your servers, with your keys or local models via Ollama.

This section walks you from a blank machine to a running console. You do not need a data-science project or a cloud AI contract to start.

**Typical path**

1. Skim [What is RAGSuite?](/GettingStarted/WhatIsRAGSuite/Index) and [Community vs Enterprise](/GettingStarted/CommunityVsEnterprise/Index) so you know what ships free.
2. Follow [Quick Start](/GettingStarted/QuickStart/Index) (or [Install with CLI](/GettingStarted/InstallCLI/Index) / [Docker](/GettingStarted/DockerDeploy/Index)).
3. Open the console on port **9191**, then configure SMTP, JWT, and URLs as needed.

<div className="rg-cta-panel">
  <p>Start here if you want the standard production-ready install path.</p>
  <div className="rg-cta-actions">
    <a className="rg-cta-primary" href="/GettingStarted/QuickStart/Index">Quick Start</a>
    <a className="rg-cta-secondary" href="/GettingStarted/InstallCLI/Index">Full CLI guide</a>
  </div>
</div>

## In this section

<CardGroup cols={2}>
  <Card title="What is RAGSuite?" icon="book-open" href="/GettingStarted/WhatIsRAGSuite/Index">
    Product overview, outcomes, and stack.
  </Card>
  <Card title="Community vs Enterprise" icon="scale" href="/GettingStarted/CommunityVsEnterprise/Index">
    What ships free vs what needs a license.
  </Card>
  <Card title="Quick Start" icon="zap" href="/GettingStarted/QuickStart/Index">
    Three CLI commands to a running stack.
  </Card>
  <Card title="Install with CLI" icon="terminal" href="/GettingStarted/InstallCLI/Index">
    Commands, ports, SMTP, and troubleshooting.
  </Card>
  <Card title="Docker deploy" icon="box" href="/GettingStarted/DockerDeploy/Index">
    `init --docker` and compose notes.
  </Card>
  <Card title="Ports & prerequisites" icon="server" href="/GettingStarted/PortsAndPrerequisites/Index">
    Ports, Node, Python, Postgres, Redis.
  </Card>
  <Card title="Configuration" icon="settings" href="/GettingStarted/Configuration/Index">
    `.env`, JWT, SMTP, and public URLs.
  </Card>
  <Card title="Doctor" icon="stethoscope" href="/GettingStarted/Doctor/Index">
    Prerequisite checks before `start`.
  </Card>
</CardGroup>

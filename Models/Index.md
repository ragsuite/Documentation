---
title: "Models overview"
description: "RAGSuite providers — OpenAI, Anthropic, Mistral, Google Gemini, or Custom LLM / Ollama with your keys."
sidebarTitle: "Models overview"
icon: "brain"
---

<div className="rg-landing-hero">
  <p className="rg-landing-eyebrow">Bring your own model</p>
  <p className="rg-landing-subtitle">
    Point RAGSuite at OpenAI, Anthropic, Mistral, Google Gemini, or fully local
    Custom LLM / Ollama. Switch per project. Your data stays on your infrastructure.
  </p>
</div>

RAGSuite is model-agnostic. You choose frontier APIs with your own keys, EU-oriented providers, or keep inference on-premise with Ollama. The product does not lock you to one vendor, and your corpus does not train someone else’s model.

**How to choose**

- Need hosted quality quickly → curated providers with **bring-your-own keys**.
- Need zero egress / air-gapped → **Ollama** (or another OpenAI-compatible local endpoint).
- Mix both → switch per project as requirements change.

<div className="rg-cta-panel">
  <p>Use curated chat and embedding catalogs — your keys, your perimeter. Local Ollama when you need air-gapped inference.</p>
  <div className="rg-cta-actions">
    <a className="rg-cta-primary" href="/Models/Providers/Index">Providers</a>
    <a className="rg-cta-secondary" href="/Models/OllamaAndAirGapped/Index">Ollama</a>
  </div>
</div>

## In this section

<CardGroup cols={2}>
  <Card title="Providers" icon="cloud" href="/Models/Providers/Index">
    OpenAI, Anthropic, Mistral, Gemini, and custom endpoints.
  </Card>
  <Card title="Ollama & air-gapped" icon="cpu" href="/Models/OllamaAndAirGapped/Index">
    Local models with no outbound LLM traffic.
  </Card>
  <Card title="Bring your own keys" icon="key" href="/Models/BringYourOwnKeys/Index">
    Store API keys on your stack — not in a shared cloud tenancy.
  </Card>
</CardGroup>

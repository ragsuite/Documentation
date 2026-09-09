---
title: "Community vs Enterprise"
description: "What ships in RAGSuite Community Edition versus Enterprise."
sidebarTitle: "CE vs EE"
---

RAGSuite is **open core**. Community Edition is a complete product. Enterprise adds organizational governance and quality/compliance tooling.

Commercial comparison: [ragsuite.de/pricing](https://www.ragsuite.de/pricing/#comparison).

## Community Edition — €0 · Apache 2.0

- Full pipeline: crawl, upload, chat (**AI Chatbot**), search (**AI Search**), widgets  
- Connectors & MCP (Gmail, MCP, Marketplace); **n8n is Beta**  
- Curated LLM providers (**OpenAI**, **Anthropic**, **Mistral**, **Google Gemini**, **Custom LLM / Ollama**)  
- REST API, API keys, webhooks  
- Citations, feedback, password auth, 2FA & sessions  
- System health, notifications, basic audit (30 days)  
- Unlimited users and unlimited projects  
- Docker / native self-hosting via [`@ragsuite/ragsuite`](https://www.npmjs.com/package/@ragsuite/ragsuite)  

No offline license key is required.

## Enterprise Edition

Requires a vendor-issued **offline key** and **Enterprise bundle**.

| Area | Notes |
|------|--------|
| SSO | Google OIDC single sign-on |
| Org RBAC | Teams, orgs, members, and project access control |
| Compare Models | Side-by-side model scoring on your infrastructure |
| Query tracing | Deep query tracing for compliance and quality review |
| Analytics | Advanced analytics |
| Audit & compliance | Full audit logs and compliance exports |
| Voice | Entitlement-gated STT/TTS on widgets |
| Mobile app | **Beta** |
| Services | White-label, SLA, CSM — by agreement |

Pricing (marketing site): **€25 / user / month**, billed annually — confirm current terms on [pricing](https://www.ragsuite.de/pricing/#comparison). Fulfillment is sales-led (`sales@ragsuite.de`).

## How to choose

- Practitioners self-hosting → start with **Community** ([Quick Start](/GettingStarted/QuickStart/Index)).  
- Need SSO, org controls, Compare Models, deeper audit/analytics → contact sales, then [Activation](/Enterprise/Activation/Index).

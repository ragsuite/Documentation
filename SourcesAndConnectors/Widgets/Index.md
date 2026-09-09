---
title: "Widgets & embeds"
description: "Embed RAGSuite AI Search and AI Chatbot widgets with citation-backed streaming answers."
sidebarTitle: "Widgets"
icon: "code"
---

**Edition:** Community

Publish AI Search and AI Chatbot where your people already work — website, intranet, or apps — as embeddable widgets. Answers stream and remain citation-backed.

## Surfaces

Product embed surfaces in Community include chat/search widget loaders (for example `/widget/v1/…`, `/search-widget/v1/…`, and `/embed/chatbot|search` paths in the CE codebase). Use the console’s embed configuration for the exact snippet for your project and environment.

## Operations notes

- Point widgets at the correct **public API base URL** for your deployment.
- Configure CSP and allowed origins for production sites.
- Align API keys / content tokens with the target project.

## Enterprise widget features

- **Voice** mic/speaker on chatbot and search widgets — Enterprise entitlement ([Voice](/Enterprise/Voice/Index))
- White-label / custom widget domain — **by agreement** (services), not a free CE module

## Related

- [AI Search](/Console/AISearch/Index)
- [AI Chatbot](/Console/AIChatbot/Index)
- [API keys & webhooks](/Platform/APIKeysAndWebhooks/Index)

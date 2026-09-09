---
title: "REST API"
description: "RAGSuite REST API — /api/v1 and interactive OpenAPI docs on port 9090."
sidebarTitle: "REST API"
icon: "code-2"
---

**Edition:** Platform / Community

When the API is running:

| Resource | URL |
|----------|-----|
| Base | `http://localhost:9090/api/v1` |
| Interactive OpenAPI | http://localhost:9090/docs |

Use the OpenAPI UI as the live contract for routes available in your installed version. Product routes live in modules; the platform provides the REST shell.

## Auth modes (summary)

- Session JWT for console users
- API keys for integrations
- Widget / content tokens for embeds

Details evolve with modules — always confirm against `/docs` on your deployment.

## Related

- [API keys & webhooks](/Platform/APIKeysAndWebhooks/Index)
- [Configuration](/GettingStarted/Configuration/Index) (`PUBLIC_API_BASE_URL`)

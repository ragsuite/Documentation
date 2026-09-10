---
title: "API keys & webhooks"
description: "Use RAGSuite API keys and webhook plumbing for integrations on the platform spine."
sidebarTitle: "API keys & webhooks"
icon: "webhook"
---

**Edition:** Platform (Community includes the practitioner surfaces that use them)

## API keys

Create and rotate API keys from the console for server-to-server access. Community auth documentation uses prefixes such as `rgs_live_*` and `rgs_test_*` — treat keys like passwords.

- Scope keys to the environments and projects that need them.
- Prefer test keys in non-production.
- Rotate after staff changes or leaks.

## Webhooks

The platform provides webhooks plumbing so your systems can react to RAGSuite events. Configure endpoints carefully (HTTPS, secrets, retry behavior) according to your security baseline.

## Widgets

Embeds may use dedicated widget headers / content tokens. See [Widgets & embeds](/SourcesAndConnectors/Widgets/Index).

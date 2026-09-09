---
description: "Use your own LLM API keys with RAGSuite — data does not train someone else’s model under product design."
sidebarTitle: "BYO keys"
---

**Edition:** Community

RAGSuite uses **your** provider credentials. Configure keys in the console / provider settings for the models you enable. Product positioning: your data stays on your infrastructure and is not used to train someone else’s model as part of RAGSuite’s design.

## Security basics

- Store secrets in `.env` / secret managers — never in git.
- Rotate keys after staff changes or suspected exposure.
- Prefer project-scoped configuration so widgets cannot call the wrong provider account.

## Internal key

`CUSTOM_LLM_INTERNAL_API_KEY` in `.env.example` is a **first-run default** for internal wiring — not a cloud vendor key. Override it in real deployments.

See [Configuration](/GettingStarted/Configuration/Index).

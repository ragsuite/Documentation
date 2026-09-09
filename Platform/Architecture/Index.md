---
title: "Architecture"
description: "High-level RAGSuite architecture — FastAPI, Expo, Postgres, Redis, ChromaDB."
sidebarTitle: "Architecture"
---

RAGSuite Community Edition is a self-hosted RAG platform:

```text
Sources (crawl · upload · connectors · MCP)
        ↓
RAGSuite (FastAPI · PostgreSQL · Redis · ChromaDB)
        ↓
Console + Widgets (AI Search · AI Chatbot)
        ↓
LLMs (OpenAI · Anthropic · Mistral · Gemini · or Custom LLM / Ollama locally)
```

## Components

| Component | Role |
|-----------|------|
| **FastAPI** | HTTP API under `/api/v1`, OpenAPI at `:9090/docs` |
| **Expo admin UI** | Operator console on `:9191` |
| **PostgreSQL** | Primary application database (`ragsuite_v3`) |
| **Redis** | Cache / jobs |
| **ChromaDB** | Vector store |
| **CLI** | `@ragsuite/ragsuite` Platform Manager |
| **Modules** | Community feature modules; Enterprise modules via licensed bundles |

## Editions

- **Platform spine** — deploy, config, auth protocol, extension loader (edition-agnostic).
- **Community modules** — practitioner pipeline (chat, search, crawl, documents, widgets, connectors, …).
- **Enterprise modules** — governance and quality loop features delivered as entitled bundles.

Owner: **NITSAN**. Product site: [ragsuite.de](https://www.ragsuite.de).

---
title: "Architecture"
description: "High-level RAGSuite architecture — FastAPI, Expo, PostgreSQL with pgvector, Redis."
sidebarTitle: "Architecture"
icon: "boxes"
---

RAGSuite Community Edition is a self-hosted RAG platform:

```text
Sources (domain crawl · sitemap XML · upload · text · Q&A pairs)
        ↓
RAGSuite (FastAPI · PostgreSQL + pgvector · Redis)
        ↓
Console + Widgets + MCP (AI Search · AI Chatbot · Admin Assistant · AI Voice Pilot · MCP hosts)
        ↓
LLMs (OpenAI · Azure OpenAI · Anthropic · Mistral · Gemini · or Custom LLM / Ollama locally)
```

## Components

| Component | Role |
|-----------|------|
| **FastAPI** | HTTP API under `/api/v1`, OpenAPI at `:9090/docs` |
| **Expo admin UI** | Operator console on `:9191` |
| **PostgreSQL** | Application database (`ragsuite_v3`) and vector store (**pgvector**, schema `ragvec`, HNSW index per collection) |
| **Redis** | Cache / jobs |
| **CLI** | `@ragsuite/ragsuite` Platform Manager |
| **Modules** | Community feature modules; Enterprise modules via licensed bundles |

## Editions

- **Platform spine** — deploy, config, auth protocol, extension loader (edition-agnostic).
- **Community modules** — practitioner pipeline (chat, search, crawl, documents, widgets, MCP, voice, AI Voice Pilot, …).
- **Enterprise modules** — governance and quality loop features delivered as entitled bundles.

Owner: **NITSAN**. Product site: [ragsuite.de](https://www.ragsuite.de).

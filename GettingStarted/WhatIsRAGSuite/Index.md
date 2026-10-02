---
title: "What is RAGSuite?"
description: "RAGSuite is a self-hosted platform for citation-backed AI Search and AI Chatbot on your infrastructure."
sidebarTitle: "What is RAGSuite?"
icon: "info"
---

RAGSuite is a **sovereign enterprise AI platform**: self-hosted or air-gapped RAG for teams that need answers grounded in their own documents — with a citation on every reply.

- **Website:** [www.ragsuite.de](https://www.ragsuite.de)  
- **Docs:** [docs.ragsuite.de](https://docs.ragsuite.de)  
- **Community source:** [github.com/ragsuite/RAGSuite](https://github.com/ragsuite/RAGSuite) (Apache License 2.0)  
- **CLI:** [`@ragsuite/ragsuite`](https://www.npmjs.com/package/@ragsuite/ragsuite) on npm  

## What you get

1. **Bring in content** — crawl a website domain or a sitemap XML, upload PDF, Office, text, and HTML files, and add written text or Q&A pairs ([Sources](/SourcesAndConnectors/Index)).  
2. **Connect AI apps and automation** — outbound [MCP](/SourcesAndConnectors/MCP/Index) for Cursor, Claude, and similar hosts; [n8n](/SourcesAndConnectors/N8n/Index) (**Beta**).  
3. **Publish where people work** — embed **AI Search** and **AI Chatbot** widgets with streaming, citation-backed answers, optionally with [Voice](/Console/Voice/Index).  
4. **Operate in the console** — use **Admin Assistant** for operator help on project history, metrics, crawl health, and configuration (separate from AI Chatbot), and [AI Voice Pilot](/Console/AIVoicePilot/Index) to speak to your knowledge base.  
5. **Improve over time** — feedback, analytics (advanced features in Enterprise), and auditability.  

## Stack

| Layer | Technology |
|-------|------------|
| API | FastAPI |
| Admin console | Expo |
| Database | PostgreSQL |
| Cache / jobs | Redis |
| Vectors | ChromaDB |
| Deploy | Native processes or Docker Compose |
| Local LLMs | Custom LLM / Ollama (optional) |

You bring your own model keys or run local models. Community Edition does not require sending your data to an external AI company.

## Open core

- **Community Edition** — complete practitioner pipeline under Apache 2.0 (including widget **Voice** and **AI Voice Pilot**).  
- **Enterprise Edition** — governance and quality features via license and bundle.  

See [Community vs Enterprise](/GettingStarted/CommunityVsEnterprise/Index).

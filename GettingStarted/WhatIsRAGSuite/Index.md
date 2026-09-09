---
description: "RAGSuite is a self-hosted platform for citation-backed AI Search and AI Chatbot on your infrastructure."
sidebarTitle: "What is RAGSuite?"
---

RAGSuite is a **sovereign enterprise AI platform**: self-hosted or air-gapped RAG for teams that need answers grounded in their own documents — with a citation on every reply.

- **Website:** [www.ragsuite.de](https://www.ragsuite.de)  
- **Docs:** [docs.ragsuite.de](https://docs.ragsuite.de)  
- **Community source:** [github.com/ragsuite/RAGSuite](https://github.com/ragsuite/RAGSuite) (Apache License 2.0)  
- **CLI:** [`@ragsuite/ragsuite`](https://www.npmjs.com/package/@ragsuite/ragsuite) on npm  

## What you get

1. **Bring in content** — crawl websites and upload PDF, DOCX, TXT.  
2. **Connect sources** — Gmail, open MCP server & client, n8n (**Beta**).  
3. **Publish where people work** — embed **AI Search** and **AI Chatbot** widgets with streaming, citation-backed answers.  
4. **Improve over time** — feedback, analytics (advanced features in Enterprise), and auditability.  

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

- **Community Edition** — complete practitioner pipeline under Apache 2.0.  
- **Enterprise Edition** — governance and quality features via license and bundle.  

See [Community vs Enterprise](/GettingStarted/CommunityVsEnterprise/Index).

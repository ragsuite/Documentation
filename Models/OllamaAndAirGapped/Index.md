---
title: "Ollama & air-gapped"
description: "Run Custom LLM / Ollama models locally — curated chat and embedding IDs, zero egress when inference stays on-prem."
sidebarTitle: "Ollama & air-gapped"
icon: "server"
---

**Edition:** Community

For air-gapped or strict-egress environments, use the **Custom LLM / Ollama** provider (default base URL typically `http://localhost:11434` via `OLLAMA_BASE_URL` in backend configuration).

## Curated models

| Role | Curated models |
|------|----------------|
| Chat | `custom-default`, `llama3:8b`, `mistral`, `gemma2`, `gemma3:27b-cloud`, `gemma4:31b-cloud` |
| Embeddings | `jina/jina-embeddings-v2-base-de` |

When the Ollama host is reachable, live discovery can surface **additional chat** models beyond this curated list. Runtime may also accept extra embeddings (for example `nomic-embed-text`, `all-minilm`, or Jina EN) that are not in the picker — see [Providers](/Models/Providers/Index).

## Why teams use this

- No model traffic leaves your servers when inference is fully local
- Aligns with sovereignty positioning: self-hosted / air-gapped, DSGVO-minded deployments
- Works with the same AI Search / AI Chatbot / widget surfaces as cloud providers

## Practical setup

1. Install and run Ollama on a host reachable from the RAGSuite API.
2. Set `OLLAMA_BASE_URL` in backend env.
3. Select **Custom LLM / Ollama** and a curated (or discovered) model in the console for the project.
4. Verify answers still cite your ingested sources (retrieval remains yours either way).

Hosted providers remain optional — your keys, your choice per project. Full curated catalogs: [Providers](/Models/Providers/Index).

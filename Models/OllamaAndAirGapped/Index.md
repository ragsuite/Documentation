---
title: "Ollama & air-gapped"
description: "Run local models with Ollama — zero egress LLM traffic when you keep inference on-prem."
sidebarTitle: "Ollama & air-gapped"
icon: "cpu"
---

**Edition:** Community

For air-gapped or strict-egress environments, run models locally with **Ollama** (default base URL typically `http://localhost:11434` via `OLLAMA_BASE_URL` in backend configuration).

## Why teams use this

- No model traffic leaves your servers when inference is fully local
- Aligns with sovereignty positioning: self-hosted / air-gapped, DSGVO-minded deployments
- Works with the same AI Search / AI Chatbot / widget surfaces as cloud providers

## Practical setup

1. Install and run Ollama on a host reachable from the RAGSuite API.
2. Set `OLLAMA_BASE_URL` in backend env.
3. Select the local model in the console for the project.
4. Verify answers still cite your ingested sources (retrieval remains yours either way).

Hosted models remain optional — your keys, your choice per project.

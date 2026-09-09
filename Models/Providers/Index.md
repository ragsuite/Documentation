---
description: "Curated LLM providers in RAGSuite — OpenAI, Anthropic, Mistral, Google Gemini, and Custom LLM / Ollama."
sidebarTitle: "Providers"
---

**Edition:** Community (`llm_providers`)

RAGSuite is **model-agnostic** within the providers below. Configure **your** API keys (or a local Ollama host) and pick chat / embedding models per project. See [Bring your own keys](/Models/BringYourOwnKeys/Index).

The console model picker uses these **curated** catalogs. Live API or Ollama discovery can add more **chat** models when keys or hosts are available.

## OpenAI

| Role | Curated models |
|------|----------------|
| Chat | `gpt-4`, `gpt-4-turbo`, `gpt-3.5-turbo`, `gpt-4o`, `gpt-4o-mini`, `gpt-4.1`, `gpt-4.1-mini`, `gpt-4.1-nano`, `gpt-5`, `gpt-5-mini`, `gpt-5-nano`, `gpt-5.1`, `gpt-5.2`, `gpt-5.4`, `gpt-5.4-pro`, `gpt-5.4-mini`, `gpt-5.4-nano`, `o3`, `o4-mini` |
| Embeddings | `text-embedding-3-large`, `text-embedding-3-small` |

## Anthropic

| Role | Curated models |
|------|----------------|
| Chat | `claude-opus-5`, `claude-sonnet-5`, `claude-haiku-4-5`, `claude-fable-5-1`, `claude-opus-4-8`, `claude-sonnet-4-6`, `claude-3-opus-20240229`, `claude-3-sonnet-20240229`, `claude-3-haiku-20240307`, `claude-3-5-sonnet-20240620` |
| Embeddings | None in the curated picker |

## Mistral

| Role | Curated models |
|------|----------------|
| Chat | `mistral-small-latest`, `ministral-3b-latest`, `ministral-8b-latest`, `ministral-14b-latest`, `mistral-medium-latest`, `mistral-large-latest`, `open-mistral-nemo`, `codestral-latest`, `codestral-2508`, `magistral-medium-latest`, `magistral-small-latest`, `labs-leanstral-1-5`, `labs-leanstral-1-5-1` |
| Embeddings | `mistral-embed` |

## Google Gemini

| Role | Curated models |
|------|----------------|
| Chat | `gemini-2.0-flash-lite`, `gemini-2.0-flash`, `gemini-2.5-flash-lite`, `gemini-2.5-flash`, `gemini-2.5-pro`, `gemini-3-flash-preview`, `gemini-3.6-flash`, `gemini-3.8-flash` |
| Embeddings | `gemini-embedding-001` |

## Custom LLM / Ollama

Local or custom inference via **Custom LLM / Ollama**. Curated chat and embedding IDs, plus setup: [Ollama & air-gapped](/Models/OllamaAndAirGapped/Index).

| Role | Curated models |
|------|----------------|
| Chat | `custom-default`, `llama3:8b`, `mistral`, `gemma2`, `gemma3:27b-cloud`, `gemma4:31b-cloud` |
| Embeddings | `jina/jina-embeddings-v2-base-de` |

## Runtime embedding extras

These may work at runtime but are **not** curated picker entries:

- OpenAI: `text-embedding-ada-002`
- Gemini: `text-embedding-004`
- Ollama: `nomic-embed-text`, `all-minilm`, and Jina EN variants

Prefer the curated embedding for each provider unless your deployment already depends on an extra.

## Enterprise quality loop

[Compare Models](/Enterprise/CompareModels/Index) runs one query across models side by side and scores answers — Enterprise feature on your infrastructure.

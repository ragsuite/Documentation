---
title: "Model Configuration"
description: "Set up AI providers once per project — chat and embedding models, API keys, and Chatbot and Search tuning."
sidebarTitle: "Model Configuration"
icon: "cpu"
---

**Edition:** Community

**Model Configuration** is where you set up AI providers once for the active project. The AI Chatbot and AI Search widgets — and source training — use the providers configured here.

## Per provider

Open a provider ([OpenAI, Anthropic, Mistral, Google Gemini, or Custom LLM / Ollama](/Models/Providers/Index)) and set:

| Setting | Notes |
|---------|-------|
| **Chat model** | Required |
| **Embedding model** | Used to train sources; chat-only providers keep each widget’s current embedding model |
| **API key** | Stored encrypted and verified with the provider when you save. Ollama runs locally and needs no key — use **Test connection** instead |
| **Chatbot tuning** | Temperature, similarity threshold, and max tokens (500–3000) for every Chatbot widget on this provider |
| **Search tuning** | Temperature, similarity threshold, and max tokens (400–3000; short answers are capped at 500) for every Search widget on this provider |

A temperature of 0.2–0.5 suits most chatbots and search: lower values keep answers focused and close to your content.

Each provider shows **Configured**, **Not configured**, or **Key rejected**. If a key is rejected, enter a valid key — until then, widgets cannot use that provider and the widget settings offer to switch to another configured provider.

## How widgets and sources use it

- In the AI Chatbot and AI Search model settings, choose one of the configured providers. Chat model, embedding model, API key, and tuning come from Model Configuration.
- When adding a website source, **AI model for training** lists the configured providers with a working key. If that provider’s model changes here, the next training uses the new model.
- **Remove configuration** deletes the saved key and model settings. Widgets already using the provider keep working until you change their provider.

## Related

- [Providers](/Models/Providers/Index)
- [BYO keys](/Models/BringYourOwnKeys/Index)
- [Ollama & air-gapped](/Models/OllamaAndAirGapped/Index)
- [Crawl](/SourcesAndConnectors/Crawl/Index)

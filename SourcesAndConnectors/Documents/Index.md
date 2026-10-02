---
title: "Documents"
description: "Upload PDF, Office, text, Markdown, and HTML documents into RAGSuite for grounded retrieval."
sidebarTitle: "Documents"
icon: "file-text"
---

**Edition:** Community

Upload the files your team already uses into a project from the **Document** tab of the console **Sources** screen. Ingested documents become retrievable context for AI Search and AI Chatbot with citations back to the source material.

| Type | Extensions |
|------|------------|
| PDF | `.pdf` |
| Word | `.doc`, `.docx` |
| PowerPoint | `.pptx` |
| Excel | `.xlsx` |
| Text and Markdown | `.txt`, `.md` |
| Web pages | `.html`, `.htm` |
| Archive | `.zip` |

Async ingest can be enabled via configuration (`ENABLE_ASYNC_DOCUMENT_INGEST` in the env template).

## Tips

- Prefer text-extractable PDFs over scanned images when possible.
- Keep sensitive corpora in appropriately access-controlled projects (Enterprise org RBAC when licensed).
- Confirm citations after bulk uploads.

## Related

- [Crawl](/SourcesAndConnectors/Crawl/Index)
- [Text & Q&A pairs](/SourcesAndConnectors/TextAndQA/Index)
- [Configuration](/GettingStarted/Configuration/Index)

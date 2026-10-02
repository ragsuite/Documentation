---
title: "Crawl"
description: "Crawl websites into RAGSuite — Domain and Sitemap XML sources for citation-backed answers."
sidebarTitle: "Crawl"
icon: "globe"
---

**Edition:** Community

Crawl brings public or allowed website content into your project so AI Search and AI Chatbot can cite it. In the console **Sources** screen, website content comes from two tabs: **Domain** and **Sitemap XML**.

## Domain

Add a website or documentation URL and choose how deep to follow links — from **This page only** up to **5 levels** (2 levels is recommended).

| Option | What it does |
|--------|--------------|
| **Allow / Deny patterns** | Include or exclude URL paths, for example `/docs/*` or `/admin/*` |
| **Retrain schedule** | **Once**, **Daily**, or **Weekly** |
| **AI model for training** | Provider set up in [Model Configuration](/Console/ModelConfiguration/Index) whose embedding model trains the pages |
| **Wait for page to fully load** | Opens each page like a browser before reading it — for modern web apps whose text appears after load (slower) |
| **Find missing pages** | Includes pages under a sub-URL (for example `example.com/docs/`) that the site links to in an unusual way |
| **Index site header / footer** | Also trains the site header (top menu) or footer; identical headers or footers are trained only once |

## Sitemap XML

Train on every page listed in a `sitemap.xml`. Enter the sitemap URL (for example `https://example.com/sitemap.xml`).

- Sitemap index files and `.xml.gz` files are supported.
- Only pages listed in the sitemap **on the same site** are trained.

Use a sitemap when your site already publishes one and you want exactly those pages — without depending on link depth.

## Guidance

- Prefer authoritative sources your organization owns or is licensed to use.
- Retrain when source sites change materially, or set a daily or weekly schedule.
- Verify citations after large crawl jobs before publishing widgets widely.

## Related

- [Documents (upload)](/SourcesAndConnectors/Documents/Index)
- [Text & Q&A pairs](/SourcesAndConnectors/TextAndQA/Index)
- [Model Configuration](/Console/ModelConfiguration/Index)
- [AI Search](/Console/AISearch/Index)

## Interactive tour

<Frame>
  <div className="rg-supademo">
    <iframe
      src="https://app.supademo.com/embed/cmu6wojy81gyzqmctl5k8o0ag"
      title="RAGSuite Sources and URLs — interactive demo"
      loading="lazy"
      allow="clipboard-write"
      allowFullScreen
    />
  </div>
</Frame>

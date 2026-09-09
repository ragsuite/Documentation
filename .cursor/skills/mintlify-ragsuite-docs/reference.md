# RAGSuite docs — authenticity reference

## Source of truth (read before writing)

| Topic | Source |
|-------|--------|
| Product positioning | https://www.ragsuite.de / https://ragsuite.de |
| Live documentation | https://docs.ragsuite.de |
| CE install / ports | `/Users/arun/RAGSUITE/README.md` |
| npm CLI | https://www.npmjs.com/package/@ragsuite/ragsuite (`@ragsuite/ragsuite`, bin `ragsuite`, v1.0.3+) |
| CLI README | `/Users/arun/RAGSUITE/cli/README.md` |
| CE vs EE modules (engineering) | `/Users/arun/RAGSUITE/docs/architecture/FEATURE-MATRIX.md` |
| License / ownership | `/Users/arun/RAGSUITE/NOTICE`, `LICENSE` |
| Security contact | `/Users/arun/RAGSUITE/SECURITY.md` → sales@ragsuite.de |
| Env template | `/Users/arun/RAGSUITE/.env.example` |
| GitHub | https://github.com/ragsuite/RAGSuite |
| npm CLI | https://www.npmjs.com/package/@ragsuite/ragsuite |
| Pricing | https://www.ragsuite.de/pricing/#comparison |

**Customer docs priority:** ragsuite.de + CE README/CLI. Do not copy internal GAPS “partial/roadmap” language into published docs when the product scope is shipped.

## CLI (customer docs)

```bash
npm install -g @ragsuite/ragsuite@latest
ragsuite init              # --yes | --docker
ragsuite doctor
ragsuite start | stop | restart
ragsuite logs [api|frontend]
ragsuite update --restart
ragsuite activate --key … --bundle … --restart   # first-time EE only
```

Install paths: `~/ragsuite`, `~/.ragsuite/config.json`.

## Design components

Use `Steps`, `Tabs`, `Tip`/`Warning`, `CardGroup`, and `.rg-landing-*` / `.rg-cta-*` from `custom.css` for overview pages.

## Product names

- **AI Search** + **AI Chatbot** (never “AI Assistant”)

## CE (document as available)

Full pipeline: crawl, upload, chat (AI Chatbot), search (AI Search), widgets.
Connectors & MCP (Gmail, MCP, Marketplace); **n8n = Beta**.
All LLM providers including local Ollama; citations; feedback; password auth; 2FA & sessions;
system health; audit basic (30 days); notifications; unlimited users/projects.
REST API, API keys, webhooks plumbing; Docker / native deploy.

## EE (requires Enterprise license + bundle)

- SSO — **Google OIDC** (shipped). Do not mention SAML or generic OIDC.
- Organization / RBAC — teams, orgs, members, project access (shipped).
- Audit full + compliance exports
- Compare Models
- Query tracing
- Analytics (advanced in EE)
- Voice (entitlement-gated)
- Mobile app = **Beta**
- White-label / SLA / CSM = by-agreement services

## Do not invent

- SCIM, SIEM streaming, usage meters as product-ready
- Public self-serve license portal
- Admin UI as “React SPA” without Expo
- Telemetry / phone-home (product claim is no telemetry)
- “AI Assistant” as a product name

## Support contacts

- Sales / security / Enterprise: **sales@ragsuite.de**
- Owner: NITSAN (https://nitsan.ai/)
- DE service partner cities (marketing site): Dresden, Berlin, Viernheim

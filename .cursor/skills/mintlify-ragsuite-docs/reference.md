# RAGSuite docs — authenticity reference

## Source of truth (read before writing)

| Topic | Source |
|-------|--------|
| Product positioning | https://www.ragsuite.de / https://ragsuite.de |
| Live documentation | https://docs.ragsuite.de |
| CE install / ports | `/Users/arun/RAGSUITE/README.md` |
| npm CLI | https://www.npmjs.com/package/@ragsuite/ragsuite (`@ragsuite/ragsuite`, bin `ragsuite`; keep customer docs version-neutral) |
| CLI README | `/Users/arun/RAGSUITE/cli/README.md` |
| CE vs EE modules (engineering) | `/Users/arun/RAGSUITE/docs/architecture/FEATURE-MATRIX.md` |
| License / ownership | `/Users/arun/RAGSUITE/NOTICE`, `LICENSE` |
| Security contact | `/Users/arun/RAGSUITE/SECURITY.md` → sales@ragsuite.de |
| Env template | `/Users/arun/RAGSUITE/.env.example` |
| LLM curated catalogs | `/Users/arun/RAGSUITE/backend/app/utils/llm_model_catalogs.py` |
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

- **AI Search** + **AI Chatbot** + **Admin Assistant** (never product name “AI Assistant”)
- **Voice (widgets)** ≠ **AI Voice Pilot** (both CE; document separately)

## CE (document as available)

Full pipeline: sources, chat (AI Chatbot), search (AI Search), widgets.
Sources tabs: **Domain** (crawl), **Sitemap XML**, **Document** (upload), **Text**, **Q&A Pairs**.
Inbound connectors (Gmail, Drive, Slack, Teams, Marketplace, …) are not shipped — do not document them.
**Admin Assistant** (in-console operator assistant — not the embeddable chatbot).
**Voice (widgets)** — browser STT/TTS on Chatbot and Search widgets.
**AI Voice Pilot** — speak-and-hear RAG (Custom voices or ElevenLabs); distinct from widget Voice.
**Model Configuration** — project-wide providers, encrypted keys, Chatbot / Search tuning.
**MCP** (Management → MCP keys / host setup); **n8n = Beta** (Integrations screen).
Curated LLM providers only: **OpenAI**, **Anthropic**, **Mistral**, **Google Gemini**,
**Custom LLM / Ollama** (with curated chat/embedding IDs — see Models/Providers).
Do not invent Azure OpenAI, Aleph Alpha, IONOS, OVHcloud, vLLM, or other vendors.
Citations; feedback; password auth; 2FA & sessions;
system health; audit basic (15 days, older events purged daily); notifications; unlimited users/projects.
REST API, API keys, webhooks plumbing; Docker / native deploy.

## EE (requires Enterprise license + bundle)

- SSO — **Google OIDC** (shipped). Do not mention SAML or generic OIDC.
- Organization / RBAC — teams, orgs, members, project access (shipped).
- Audit full — unlimited history + CSV/JSON export
- Compliance — per-project data retention (Settings › Data Retention)
- Compare Models
- Query tracing
- Analytics (advanced in EE)
- White label — custom chatbot title, header logo, disclaimer; hide console system footer
- Mobile app = **Beta**
- SLA / CSM = by-agreement services

## Do not invent

- Extra LLM cloud vendors beyond the five curated providers (no Azure OpenAI, Aleph Alpha, IONOS, OVHcloud, vLLM as shipped configs)
- Model IDs not in the curated catalogs / user-approved lists (except documenting live discovery and named runtime embedding extras)
- SCIM, SIEM streaming, usage meters as product-ready
- Public self-serve license portal
- Admin UI as “React SPA” without Expo
- Telemetry / phone-home (product claim is no telemetry)
- “AI Assistant” as a customer-facing product name (use **Admin Assistant**)

## Support contacts

- Sales / security / Enterprise: **sales@ragsuite.de**
- Owner: NITSAN (https://nitsan.ai/)
- DE service partner cities (marketing site): Dresden, Berlin, Viernheim

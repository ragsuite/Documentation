---
title: "Configuration"
description: "Configure RAGSuite secrets, SMTP, and URLs in .env for CLI or clone installs."
sidebarTitle: "Configuration"
---

Set secrets once, then restart the stack. **Never commit `.env`.**

## Where the file lives

| Install type | Path |
|--------------|------|
| CLI (default) | `~/ragsuite/.env` |
| Git clone | repo root `.env` (from `.env.example`) |

```bash
# clone installs
cp .env.example .env
```

`ragsuite init` creates and manages env for CLI installs. It regenerates `JWT_SECRET_KEY`.

## Required secrets

| Variable | Purpose |
|----------|---------|
| `JWT_SECRET_KEY` | Session/JWT signing — use a long random secret in production |
| `CUSTOM_LLM_INTERNAL_API_KEY` | First-run default internal key (not a cloud vendor key). Override anytime |

## Email (SMTP)

Needed for invites, forgot-password, and 2FA email. Smoke SMTP from `init` may let the API start but **does not** deliver real mail.

```bash
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=you@gmail.com
SMTP_PASSWORD=your-16-char-app-password
SMTP_USE_TLS=true
EMAIL_FROM=you@gmail.com
```

Then:

```bash
ragsuite restart
# or from a clone: npm run stop && npm start
```

## Frontend / API URLs

| Variable | Typical local value |
|----------|---------------------|
| `FRONTEND_API_URL` | `http://localhost:9090` (baked into Docker frontend build) |
| `FRONTEND_BASE_URL` | `http://localhost:9191` |
| `PUBLIC_API_BASE_URL` | `http://localhost:9090/api/v1` |
| `CORS_ORIGINS` | Your console origin(s) |

## Other common flags

| Variable | Notes |
|----------|-------|
| `DEBUG` | Development verbosity |
| `HF_HUB_OFFLINE` | Prefer offline Hugging Face hub behavior when set |
| `SSO_ENABLED` | SSO is **Enterprise**; keep `false` on Community unless EE is attached |
| `ENABLE_ASYNC_DOCUMENT_INGEST` | Async document ingest |
| `RAGSUITE_EE_ROOT` | Absolute path to EE tree when attaching Enterprise for Docker DX |

Backend settings (database URL, Redis, Chroma, `OLLAMA_BASE_URL`) live in the backend env template in the Community repository.

## After changes

Restart so the API reloads configuration. Rotate secrets after any shared or compromised install — see [Security policy](/SecurityAndTrust/SecurityPolicy/Index).

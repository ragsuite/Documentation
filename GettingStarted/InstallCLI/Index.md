---
title: "Install CLI"
description: "Install RAGSuite Community Edition with the official Platform Manager CLI @ragsuite/ragsuite."
sidebarTitle: "Install CLI"
icon: "terminal"
---

The official **Platform Manager CLI** is published on npm as [`@ragsuite/ragsuite`](https://www.npmjs.com/package/@ragsuite/ragsuite) (current release **1.0.3**). It installs and runs Community Edition on your machine. **Community needs no offline license key.**

```bash
npm install -g @ragsuite/ragsuite@latest
ragsuite init
ragsuite start
```

| Mode | Web UI | How it runs |
|------|--------|-------------|
| **native** (default) | http://localhost:**9191** | Host processes |
| **docker** (`init --docker`) | http://localhost:**9191** | Docker Compose |

API: http://localhost:**9090** · OpenAPI: http://localhost:**9090/docs**

Default install folder: `~/ragsuite`  
Saved config: `~/.ragsuite/config.json`

<Tip>
Prefer Node.js **20** or **22** LTS for the CLI and local tooling. The package requires Node **18+**.
</Tip>

## Quick start

<Steps>
  <Step title="Install the CLI">
```bash
npm install -g @ragsuite/ragsuite@latest
ragsuite version
```
  </Step>
  <Step title="Initialize">
```bash
ragsuite init              # prompts for mode; default = native
# ragsuite init --yes      # native, non-interactive
# ragsuite init --docker   # Docker mode
```
  </Step>
  <Step title="Check prerequisites">
```bash
ragsuite doctor
```
  </Step>
  <Step title="Start">
```bash
ragsuite start
```

Open the console at `http://localhost:9191` and the API at `http://localhost:9090`.
  </Step>
</Steps>

```bash
ragsuite logs              # all
ragsuite logs api
ragsuite logs frontend

ragsuite stop              # keeps database
```

## Everyday commands

| Command | What it does |
|---------|----------------|
| `init` | First install; choose native or docker |
| `start` / `stop` / `restart` | Run the stack (`stop` keeps data) |
| `logs [api\|frontend]` | Follow logs |
| `doctor` | Check prerequisites |
| `update` | Upgrade Community (+ optional Enterprise steps) |
| `version` | Print CLI version |
| `status` | Install path, key, active Enterprise bundle |
| `extensions` / `plugins` | List modules on disk |
| `license status` | Check offline key |
| `bundle list` | List installed Enterprise bundles |
| `activate` | **First-time** Enterprise only |

```bash
ragsuite status
ragsuite extensions
ragsuite license status
ragsuite bundle list
```

## Upgrade Community

```bash
ragsuite update --restart
```

This command:

1. Upgrades the global CLI  
2. Pulls Community into your install folder  
3. Keeps database, `.env`, and any existing offline key  
4. Does **not** wipe volumes  

<Warning>
Do **not** use `docker compose down -v` or `init --force` for normal upgrades — those paths destroy data or reinstall aggressively.
</Warning>

## Ports

| Service | native | docker |
|---------|--------|--------|
| API | **9090** | **9090** |
| Web | **9191** (Expo) | **9191** (nginx) |
| Postgres | **5436** | **5436** |
| Redis | **6382** | **6382** |
| Chroma | **8004** | internal |

## Email (SMTP)

`init` may write **smoke** SMTP so the API can start. Smoke values do **not** deliver real mail.

Set real SMTP in `~/ragsuite/.env`:

```bash
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=you@gmail.com
SMTP_PASSWORD=your-16-char-app-password
SMTP_USE_TLS=true
EMAIL_FROM=you@gmail.com
```

Then: `ragsuite restart`  
Never commit `.env`.

## Enterprise

Community needs no key. First-time Enterprise always uses `ragsuite activate` — not `update`. Full steps: [Enterprise activation](/Enterprise/Activation/Index).

## Troubleshooting

| Issue | Fix |
|-------|-----|
| `command not found` | `npm install -g @ragsuite/ragsuite@latest` |
| Wrong UI port | native / docker → **9191** |
| Port 9090 busy | `ragsuite stop` |
| `/docs` missing | `ragsuite restart` after update |
| Postgres/Redis down (native) | Start services, or install Docker and `start` again |
| Docker daemon down | Start Docker Desktop, then `doctor` |
| Mail / invites fail | Set real `SMTP_*` + `EMAIL_FROM`, then `restart` |
| `update` refuses first Enterprise | Use `activate --key … --bundle …` |
| `Bundle not found` | Place the emailed `.encbundle` (+ `manifest.enc.json`) at `<install>/`, or pass an absolute path. Do not unpack by hand. |
| Key expired / EE refused | `update --key "<install>/.ragsuite/license/offline.key" --restart` |
| Refuses to overwrite a valid key | Intended — add `--force` only if your vendor says so |

## Package

- npm: [npmjs.com/package/@ragsuite/ragsuite](https://www.npmjs.com/package/@ragsuite/ragsuite)  
- Source: [github.com/ragsuite/RAGSuite/tree/main/cli](https://github.com/ragsuite/RAGSuite/tree/main/cli)  
- License: Apache 2.0 (Community CLI)

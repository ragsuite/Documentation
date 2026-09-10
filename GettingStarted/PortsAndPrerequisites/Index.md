---
title: "Ports & prereqs"
description: "Ports and tool versions for RAGSuite native and Docker installs."
sidebarTitle: "Ports & prereqs"
icon: "network"
---

Requirements match the official Platform Manager CLI ([`@ragsuite/ragsuite`](https://www.npmjs.com/package/@ragsuite/ragsuite)).

## Ports

| Service | Native | Docker |
|---------|--------|--------|
| API | **9090** | **9090** |
| Web | **9191** (Expo) | **9191** (nginx) |
| Postgres | **5436** | **5436** |
| Redis | **6382** | **6382** |
| Chroma | **8004** | internal |

OpenAPI when the API is up: http://localhost:9090/docs

<Warning>
If another service already binds **9090**, **9191**, **5436**, **6382**, or **8004**, `ragsuite start` and `ragsuite doctor` will fail until you free those ports or change the conflicting service. Do not guess alternate ports unless you also update `.env` consistently.
</Warning>

## Shared (CLI)

| Tool | Version |
|------|---------|
| Node.js | **18+** (20/22 LTS recommended) |
| npm | ships with Node |
| Git | 2.30+ |
| OS | macOS, Linux, or Windows **WSL2 / Git Bash** |

## Native mode

| Tool | Note |
|------|------|
| Python | **3.14** (`python3.14`) |
| Yarn | **1.22+** (`corepack enable`) |
| Postgres | **15+** on **:5436**, database `ragsuite_v3` |
| Redis | **7+** on **:6382** |
| Docker | optional — can start Postgres/Redis only |

## Docker mode

| Tool | Note |
|------|------|
| Docker Desktop / Engine | daemon running |
| Compose v2 | `docker compose version` |

## Verify

```bash
ragsuite doctor
# from a clone:
bash scripts/doctor.sh
```

See [Doctor](/GettingStarted/Doctor/Index).

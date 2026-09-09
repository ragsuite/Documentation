---
description: "Verify RAGSuite prerequisites with ragsuite doctor before you start the stack."
sidebarTitle: "Doctor"
---

`ragsuite doctor` checks that your machine meets the requirements for the install mode you chose (`native` or `docker`).

## CLI (recommended)

```bash
ragsuite doctor
```

Run this after `init`, and again whenever Node, Python, Postgres, Redis, or Docker changes.

## From a git clone

```bash
bash scripts/doctor.sh
```

## What to fix first

1. **Postgres** on **5436** with database `ragsuite_v3` (native mode)  
2. **Redis** on **6382**  
3. **Node.js 18+** (20/22 LTS recommended); native mode also needs **Python 3.14** and Yarn **1.22+**  
4. **Docker mode:** daemon running and Compose v2 (`docker compose version`)

Full matrix: [Ports & prerequisites](/GettingStarted/PortsAndPrerequisites/Index).

## Status helpers

```bash
ragsuite status
ragsuite logs api
ragsuite logs frontend
```

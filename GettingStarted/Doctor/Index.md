---
title: "Doctor"
description: "Verify RAGSuite prerequisites with ragsuite doctor before you start the stack."
sidebarTitle: "Doctor"
icon: "heart-pulse"
---

`ragsuite doctor` checks that your machine meets the requirements for the install mode you chose (`native` or `docker`).

<Tip>
Run `ragsuite doctor` after `init`, and again whenever Node, Python, Postgres, Redis, Chroma, or Docker changes.
</Tip>

## CLI (recommended)

```bash
ragsuite doctor
```

## From a git clone

```bash
bash scripts/doctor.sh
```

## What to fix first

<Steps>
  <Step title="Postgres">
    Native mode needs Postgres on **5436** with database `ragsuite_v3`.
  </Step>
  <Step title="Redis">
    Confirm Redis listens on **6382**.
  </Step>
  <Step title="Chroma">
    Native mode expects Chroma on **8004**. Docker mode keeps Chroma internal to Compose.
  </Step>
  <Step title="Runtime tools">
    Use **Node.js 18+** (20/22 LTS recommended). Native mode also needs **Python 3.14** and Yarn **1.22+**.
  </Step>
  <Step title="Docker mode">
    If you chose Docker, confirm the daemon is running and Compose v2 works (`docker compose version`).
  </Step>
</Steps>

Full matrix: [Ports & prerequisites](/GettingStarted/PortsAndPrerequisites/Index).

## Status helpers

```bash
ragsuite status
ragsuite logs api
ragsuite logs frontend
```

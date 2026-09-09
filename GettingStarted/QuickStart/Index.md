---
description: "Install RAGSuite Community Edition in minutes with the official CLI — or run from a git clone."
sidebarTitle: "Quick Start"
---

Get a running Community Edition console on your infrastructure. **No offline license key is required.**

## Recommended: Platform Manager CLI

Published package: [`@ragsuite/ragsuite`](https://www.npmjs.com/package/@ragsuite/ragsuite) (v**1.0.3**).

<Steps>
  <Step title="Install">
```bash
npm install -g @ragsuite/ragsuite@latest
ragsuite version
```
  </Step>
  <Step title="Initialize">
```bash
ragsuite init              # default = native
# ragsuite init --docker   # optional Docker mode
# ragsuite init --yes      # native, non-interactive
```
  </Step>
  <Step title="Verify and start">
```bash
ragsuite doctor
ragsuite start
```
  </Step>
</Steps>

| Surface | URL |
|---------|-----|
| Console (web) | http://localhost:**9191** |
| API | http://localhost:**9090** |
| OpenAPI | http://localhost:**9090/docs** |

```bash
ragsuite logs
ragsuite stop              # keeps the database
```

Default install: `~/ragsuite` · Config: `~/.ragsuite/config.json`

Full command reference: [Install with CLI](/GettingStarted/InstallCLI/Index).

<Tabs>
  <Tab title="Native (default)">
Host processes. Requires Postgres on **:5436** (`ragsuite_v3`), Redis on **:6382**, Node 18+, and for native mode Python **3.14** + Yarn 1.22+. See [Ports & prerequisites](/GettingStarted/PortsAndPrerequisites/Index).
  </Tab>
  <Tab title="Docker">
```bash
ragsuite init --docker
ragsuite doctor
ragsuite start
```
Requires Docker Engine/Desktop and Compose v2. See [Docker deploy](/GettingStarted/DockerDeploy/Index).
  </Tab>
</Tabs>

<Warning>
Do not run native and Docker stacks at the same time on the same ports.
</Warning>

## Alternative: git clone (developers)

From the Community repository:

```bash
cp .env.example .env    # once — set JWT, SMTP, and secrets
npm start               # API :9090 · web :9191
npm run stop            # stops processes; does not wipe the database
```

Check prerequisites with `bash scripts/doctor.sh` or [Doctor](/GettingStarted/Doctor/Index).

## Next steps

- [Configuration](/GettingStarted/Configuration/Index) — JWT, SMTP, URLs  
- [Console](/Console/Index) — AI Search and AI Chatbot  
- [Community vs Enterprise](/GettingStarted/CommunityVsEnterprise/Index)

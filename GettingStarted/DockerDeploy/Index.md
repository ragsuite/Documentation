---
description: "Run RAGSuite with Docker via the official CLI or docker compose from a clone."
sidebarTitle: "Docker"
---

Docker is an optional deploy mode. For most Community installs, use the CLI with `--docker`. Native remains the default when you run `ragsuite init` without flags.

## Recommended: CLI

```bash
npm install -g @ragsuite/ragsuite@latest
ragsuite init --docker
ragsuite doctor
ragsuite start
```

| Surface | URL |
|---------|-----|
| Console | http://localhost:**9191** |
| API | http://localhost:**9090** |
| OpenAPI | http://localhost:**9090/docs** |

```bash
ragsuite logs
ragsuite stop              # keeps volumes / database
```

## From a repository clone

```bash
cp .env.example .env
npm run start:docker    # or: docker compose up -d --build
npm run down            # stops containers; volumes kept
```

<Warning>
Never use `docker compose down -v` unless you intend to **delete** data volumes. Prefer `ragsuite stop` or `npm run down` for routine shutdowns.
</Warning>

Do **not** run Docker and native stacks on the same host ports at the same time.

### ChromaDB stuck unhealthy

If ChromaDB is unhealthy and you want to avoid rebuilding the frontend:

```bash
docker compose up -d --no-deps --force-recreate chromadb
docker compose up -d
```

## Ports (Docker)

| Service | Port |
|---------|------|
| API | **9090** |
| Web (nginx) | **9191** |
| Postgres | **5436** |
| Redis | **6382** |
| Chroma | internal |

See [Ports & prerequisites](/GettingStarted/PortsAndPrerequisites/Index) and [Install with CLI](/GettingStarted/InstallCLI/Index).

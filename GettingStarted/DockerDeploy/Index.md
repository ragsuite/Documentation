---
title: "Docker"
description: "Run RAGSuite with Docker via the official CLI or docker compose from a clone."
sidebarTitle: "Docker"
icon: "box"
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

## Vector store

Vectors live in the same PostgreSQL database with the **pgvector** extension. The Compose Postgres image includes pgvector, and the existing `postgres_data` volume is reused — there is no separate vector database container.

## Upgrading from a Chroma-based release

Releases **1.0.7 and earlier** stored vectors in ChromaDB. The first start after upgrading runs a one-time **`vector-migrate`** step that imports that data into pgvector and verifies every row before the API starts.

<Steps>
  <Step title="Back up">
    From your install folder (`~/ragsuite` for CLI installs), back up the database and the old vector data before upgrading:

    ```bash
    pg_dump "$DATABASE_URL" > backup.sql
    tar -czf chroma_db-backup.tar.gz backend/data/chroma_db
    ```
  </Step>
  <Step title="Start with the full command">
    Run `ragsuite update --restart` (or `docker compose up -d --build` from a clone). Do **not** use `--no-deps backend` for this first start — the API would start before the import.
  </Step>
  <Step title="Check the import">
    In Docker mode:

    ```bash
    ragsuite logs vector-migrate
    # or: docker compose logs vector-migrate
    ```

    The log should end with `migration complete: N collection(s), M rows`. Later starts report `already migrated` and skip the step. If verification fails, the API stays down and the old data is untouched — fix the cause and start again; the import resumes.
  </Step>
  <Step title="Clean up">
    After you have verified answers in the console, delete `backend/data/chroma_db`, then run `docker compose up -d --remove-orphans` to remove the old `chromadb` container.
  </Step>
</Steps>

<Info>
**Native installs** run the same import during `ragsuite start`, before the API starts, and print the result in the start output. Host Postgres must have pgvector installed, and you must run `CREATE EXTENSION vector;` once as a superuser in the RAGSuite database. If your old vector data is in a non-default location, set `CHROMA_PERSIST_PATH` (native) or `CHROMA_HOST_PERSIST_PATH` (Docker) before the first start.
</Info>

## Ports (Docker)

| Service | Port |
|---------|------|
| API | **9090** |
| Web (nginx) | **9191** |
| Postgres | **5436** |
| Redis | **6382** |

See [Ports & prerequisites](/GettingStarted/PortsAndPrerequisites/Index) and [Install with CLI](/GettingStarted/InstallCLI/Index).

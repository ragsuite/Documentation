---
title: "Enterprise activation"
description: "Activate RAGSuite Enterprise with offline.key and encbundle using the Platform Manager CLI."
sidebarTitle: "Activation"
icon: "key-round"
---

**Community Edition needs no key.** Enterprise is sales-led: your vendor emails three files. Place them in your install root (default `~/ragsuite`). Do **not** unpack the `.encbundle`. Do not hand-edit the key.

| File | Path | Command |
|------|------|---------|
| `offline.key` | `<install>/.ragsuite/license/offline.key` | First time: `activate`. Renew: `update --key` |
| `ragsuite-ee-<version>.encbundle` | `<install>/ragsuite-ee-<version>.encbundle` | First time: `activate`. Later: `update --bundle` |
| `manifest.enc.json` | `<install>/manifest.enc.json` | Keep next to the `.encbundle` |

The CLI validates the key and bundle and installs Enterprise modules. Database and `.env` are never wiped.

## 1. First-time — always `activate`

```bash
ragsuite activate \
  --key "<install>/.ragsuite/license/offline.key" \
  --bundle "<install>/ragsuite-ee-<ver>.encbundle" \
  --restart
```

Equivalent alias:

```bash
ragsuite ee-activate \
  "<install>/.ragsuite/license/offline.key" \
  --bundle "<install>/ragsuite-ee-<ver>.encbundle" \
  --restart
```

Works for **native and Docker**. `--restart` rebuilds/restarts so the API loads the key and bundle.

<Warning>
`update` **cannot** install Enterprise for the first time. If you run `update --key` or `update --bundle` with no key yet, the CLI refuses and tells you to use `activate`.
</Warning>

## 2. Later Enterprise code — `update --bundle`

Keep your current key. Place the new encbundle and matching `manifest.enc.json` at `<install>/`, then:

```bash
ragsuite update --bundle "<install>/ragsuite-ee-<ver>.encbundle" --restart
```

If the installed key is **expired**, Enterprise is not updated (Community update can still run). Renew the key first.

## 3. Renew expired key — `update --key`

Paste the new key over `<install>/.ragsuite/license/offline.key` (a previous key must already exist from `activate`):

```bash
ragsuite update --key "<install>/.ragsuite/license/offline.key" --restart
```

- Expired or invalid installed key → replacement proceeds  
- Still-valid installed key → needs `--force` (vendor/support only)  
- Optional combined renew + pack:  

```bash
ragsuite update \
  --key "<install>/.ragsuite/license/offline.key" \
  --bundle "<install>/ragsuite-ee-<ver>.encbundle" \
  --restart
```

## Status

```bash
ragsuite status
ragsuite license status
ragsuite bundle list
```

Questions: [sales@ragsuite.de](mailto:sales@ragsuite.de) · CLI package: [`@ragsuite/ragsuite`](https://www.npmjs.com/package/@ragsuite/ragsuite)

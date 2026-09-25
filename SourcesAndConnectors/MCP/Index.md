---
title: "MCP"
description: "Connect AI apps to RAGSuite with MCP keys — Cursor, Claude, VS Code, Windsurf, ChatGPT, and more."
sidebarTitle: "MCP"
icon: "plug"
---

**Edition:** Community

**MCP** (Model Context Protocol) lets the AI apps you use talk **to** RAGSuite on your infrastructure. In the console open **Management → MCP**.

This is **not** [Connectors](/SourcesAndConnectors/Connectors/Index) (inbound Gmail, Drive, Slack, Teams, and related Sources sync). It is also not the general REST [API keys & webhooks](/Platform/APIKeysAndWebhooks/Index) surface used for widgets and HTTP automation — MCP keys are issued specifically for MCP hosts.

## Keys

On the **Keys** tab:

- Create a named MCP key (the full secret is shown **once** — copy it immediately).
- Turn keys on or off, or delete keys that should stop working.
- A key connects AI apps to the projects you can open.

## Connect

On the **Connect** tab:

1. Choose an active key.
2. Pick a host: **Cursor**, **Claude**, **Manus**, **VS Code**, **Windsurf**, **ChatGPT**, or **Other**.
3. Copy the setup snippet for that host and paste it into the host’s MCP / connector settings.

Typical endpoint shape (replace with your public API base):

```json
{
  "mcpServers": {
    "ragsuite": {
      "url": "https://<your-api-host>/api/v1/mcp/",
      "headers": {
        "Authorization": "Bearer <your-mcp-key>"
      }
    }
  }
}
```

Use a reachable API URL for remote hosts (local `localhost` only works on the same machine). If you expose the API through a tunnel, include any public-link helper fields the Connect tab shows.

### Host setup (high level)

| Host | What to do |
|------|------------|
| **Cursor** | Settings → MCP → add connection → paste setup → save |
| **Claude** | Desktop Developer config → paste setup into the Claude config file |
| **VS Code / Windsurf** | Add the MCP server entry from the Connect snippet |
| **Manus** | Add a web connection and paste setup (do not use the sign-in button) |
| **ChatGPT** | Add a custom connector using the Connect snippet |
| **Other** | Use the generic MCP URL + Bearer key from Connect |

Exact menu labels vary by host version — follow the numbered steps shown in the console for the selected host.

## Related

- [Connectors](/SourcesAndConnectors/Connectors/Index)
- [API keys & webhooks](/Platform/APIKeysAndWebhooks/Index)
- [Widgets](/SourcesAndConnectors/Widgets/Index)

# Installing Brush Pack (remote MCP server, no install needed)

Brush Pack is a hosted remote MCP server. There is nothing to download, build or run, and no API key.

Add this to the MCP settings file (in Cline: MCP Servers, Configure, then cline_mcp_settings.json):

```json
{
  "mcpServers": {
    "brush-pack": {
      "type": "streamableHttp",
      "url": "https://brush-pack.nerolabs.workers.dev/mcp",
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

Save the file. The server's tools appear straight away. To check it works, ask for the server's capabilities (the `list_capabilities` tool).

Docs: https://brush-pack.nerolabs.workers.dev/docs

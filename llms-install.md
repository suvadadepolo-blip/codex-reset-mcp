# Installing the Codex Reset MCP server

The server is hosted; there is nothing to download, build or run.

1. Add a remote MCP server named `codex-reset` with the URL `https://codex-reset.com/mcp`.
2. Transport is Streamable HTTP. No API key, no environment variables, no auth headers.
3. For a client configured through `cline_mcp_settings.json` or a similar `mcpServers` file, use:

```json
{
  "mcpServers": {
    "codex-reset": {
      "type": "streamableHttp",
      "url": "https://codex-reset.com/mcp"
    }
  }
}
```

4. If the client only supports stdio servers, wrap the URL instead:

```json
{
  "mcpServers": {
    "codex-reset": {
      "command": "npx",
      "args": ["-y", "mcp-remote", "https://codex-reset.com/mcp"]
    }
  }
}
```

5. Confirm the install by calling `get_reset_forecast`; it takes no required arguments.

Tools: `get_reset_forecast`, `get_reset_timeline`, `get_codex_status`. All read-only.

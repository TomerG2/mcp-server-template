# mcp-server template

MCP (ModelContextProvider) server template

---

## Building locally

To build the container image locally using Podman, run:

```sh
podman build -t mcp-server:latest .
```

This will create a local image named `mcp-server:latest` that you can use to run the server.

## Running with Podman or Docker

Example configuration for running with Podman:

```json
{
  "mcpServers": {
    "mcp-server": {
      "command": "podman",
      "args": [
        "run",
        "-i",
        "--rm",
        "-e", "API_BASE",
        "-e", "API_KEY",
        "localhost/mcp-server:latest"
      ],
      "env": {
        "API_BASE": "https://api.example.com",
        "API_KEY": "REDACTED"
      }
    }
  }
}
```

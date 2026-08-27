# mcp-get-registry

The official registry of MCP servers for the [`mcp-get`](https://github.com/m-usmanashraf/mcp-get) CLI.

## Adding a new MCP server

We happily accept PRs adding new MCP servers to the registry.

1. Fork this repo
2. Add a new entry to the `servers` array in [`servers.json`](./servers.json)
3. Open a PR

## Entry format

```json
{
  "name": "your-server-name",
  "description": "Short one-line description of what the server does.",
  "runtime": "node",
  "package": "@your-org/mcp-server-package",
  "homepage": "https://github.com/your-org/your-server-repo"
}
```

### Field guide

| Field | Description |
|-------|-------------|
| `name` | Unique short name used with `mcp-get install <name>`. Lowercase, hyphens only. |
| `description` | One clear sentence explaining what the server does. |
| `runtime` | `node` (launched with `npx`) or `python` (launched with `uvx`). |
| `package` | The npm package name or PyPI package name. |
| `homepage` | Link to the server's source repo or documentation. |

## Quality guidelines

- Only submit MCP servers that are **published and installable** (npm / PyPI).
- Servers must be **actively maintained** (commit within the last 6 months).
- Descriptions must be **honest** — no marketing language or claims that overstate capabilities.
- **No duplicates** — search existing entries first.

## Reporting a bad entry

If a server is broken, unmaintained, or malicious, open an issue. We remove entries quickly.

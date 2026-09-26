# MCP Config Guard - agent config lint

Reads .mcp.json / .vscode/mcp.json / claude_desktop_config.json while you edit it and marks the lines that hand an AI agent more than you meant - unpinned servers, literal credentials, plaintext transport, whole-home filesystem roots. 23 rules, offline, no server is ever started.

## Install

```
npx @readystack/mcp-config-guard file
```

Node 18+. The same 23 rules as the VS Code extension, from a terminal or CI.

## Free

- Check the MCP config file you have open against all 23 rules - the line number, one sentence on what goes wrong, and the line that replaces it - offline, no key, no limit.
- `--rules` lists every rule

## With a licence ($29 once)

- Scale and hand-off: one sweep over every MCP config in the workspace and in the client config folders, a dated CSV/JSON/HTML report, and machine-readable output a CI step can fail on.

```
@readystack/mcp-config-guard --dir ./templates --report html --out report.html
```

Upwork lists cybersecurity developers at a $60 median hourly rate, $40-$90 typical (Sept 2026).

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "mcp-config-guard": { "command": "npx", "args": ["-y", "@readystack/mcp-config-guard", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence; the full sweep is free for 7 days). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: MCP Config Guard - agent config lint
  run: npx -y @readystack/mcp-config-guard --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/mcp-config-guard --dir /work --ci`)

Try the full run free for 7 days — no key needed. Then one licence, 7-day refund, no questions. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_qkyHZkQQW6eB0rXgrKfDGviLlVixnkbP42q8B3h7YrG)


<!-- mcp config guard -->

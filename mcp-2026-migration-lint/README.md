# MCP 2026 Migration Lint

The 2026-07-28 MCP revision removed the initialize handshake, sessions, ping and 4 more RPCs. 27 rules find them in your mcp.json and server code, with the replacement on each line.

## Install

```
npx @readystack/mcp-2026-migration-lint file
```

Node 18+. The same 27 rules as the VS Code extension, from a terminal or CI.

## Free

- All 27 rules on the file you have open, or on just the lines you select, with the line number and the replacement for each - no key, no account, offline.
- `--rules` lists every rule

## With a licence ($29 once)

- Scale, not a better answer: every mcp.json and server file in the whole repository in one pass, the findings exported as CSV/JSON/HTML, and CI output that fails the build.

```
@readystack/mcp-2026-migration-lint --dir ./templates --report html --out report.html
```

Freelance senior software engineers publish an average of $101/hour (contractrates.fyi, 2026, 584 submissions).

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "mcp-2026-migration-lint": { "command": "npx", "args": ["-y", "@readystack/mcp-2026-migration-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: MCP 2026 Migration Lint
  run: npx -y @readystack/mcp-2026-migration-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/mcp-2026-migration-lint --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_oDjtHoT9LT11eZ3znaYEtjljb5fL8onpd7R0j3VkVqB)


<!-- mcp -->

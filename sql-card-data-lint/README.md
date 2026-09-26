# SQL Card Data Lint (PCI DSS Req 3)

Names every column, index, view and seed row in a .sql migration that stores card data, with its PCI DSS Requirement 3 rule id

## Install

```
npx @readystack/sql-card-data-lint file
```

Node 18+. The same 10 rules as the VS Code extension, from a terminal or CI.

## Free

- Check the .sql file open in your editor against all 10 rules and get every card-data column, index, view and seed literal with its Requirement 3 rule id and a replacement line
- `--rules` lists every rule

## With a licence ($29 once)

- Sweep every migration in the workspace at once and write a dated findings report you keep and hand to an assessor, for team and commercial use

```
@readystack/sql-card-data-lint --dir ./templates --report html --out report.html
```

A QSA-led gap analysis of your data stores is commonly quoted as a five-figure engagement; the same migrations are read here in the editor.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "sql-card-data-lint": { "command": "npx", "args": ["-y", "@readystack/sql-card-data-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: SQL Card Data Lint (PCI DSS Req 3)
  run: npx -y @readystack/sql-card-data-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/sql-card-data-lint --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_HL23mfuzaP3RMTfsQGzbUYmVSiTyJBd8Czg9B1TIuJT)


<!-- sql card data lint -->

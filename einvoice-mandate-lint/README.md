# E-Invoice Mandate Lint - EU 2026

Lints UBL and CII invoice XML against EN 16931 and the national e-invoicing mandates that are live in 2026

## Install

```
npx @readystack/einvoice-mandate-lint file
```

Node 18+. The same 35 rules as the VS Code extension, from a terminal or CI.

## Free

- Lint the invoice XML you have open - every EN 16931 core field plus the country mandate rules its CustomizationID and seller country select, reported with line numbers.
- `--rules` lists every rule

## With a licence ($29 once)

- Scan every invoice XML in the workspace in one pass and export the findings as JSON, CSV or SARIF you keep and run in CI.

```
@readystack/einvoice-mandate-lint --dir ./templates --report html --out report.html
```

An EN 16931 / Peppol integration consultant reviews an invoice mapping at about $170 an hour.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "einvoice-mandate-lint": { "command": "npx", "args": ["-y", "@readystack/einvoice-mandate-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: E-Invoice Mandate Lint - EU 2026
  run: npx -y @readystack/einvoice-mandate-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/einvoice-mandate-lint --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_V1RBWcrS00NsYLx6EMXeji1xvbix6LF1yO9qR4DduBz)


<!-- einvoice mandate lint -->

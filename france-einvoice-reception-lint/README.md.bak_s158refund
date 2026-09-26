# France E-Invoice Reception Lint

12 checks for the French mandatory mentions a PDP rejects, on Factur-X, UBL and CII invoices

## Install

```
npx @readystack/france-einvoice-reception-lint file
```

Node 18+. The same 12 rules as the VS Code extension, from a terminal or CI.

## Free

- Check the invoice XML open in the editor against all 12 rules and get every finding with line numbers — a finished answer for that file, no key
- `--rules` lists every rule

## With a licence ($29 once)

- Sweep every invoice in the workspace and write one dated reception-readiness report — the same 12 rules at workspace scope

```
@readystack/france-einvoice-reception-lint --dir ./templates --report html --out report.html
```

An e-invoicing integrator bills about 95 US dollars an hour to map and re-test one invoice profile

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "france-einvoice-reception-lint": { "command": "npx", "args": ["-y", "@readystack/france-einvoice-reception-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence; the full sweep is free for 7 days). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: France E-Invoice Reception Lint
  run: npx -y @readystack/france-einvoice-reception-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/france-einvoice-reception-lint --dir /work --ci`)

Try the full run free for 7 days — no key needed. Then one licence, 7-day refund, no questions. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_a6x1aVkUPqSGx38DFlJw68NPUQdMdCYBpENCR47YuFw)


<!-- france einvoice reception lint -->

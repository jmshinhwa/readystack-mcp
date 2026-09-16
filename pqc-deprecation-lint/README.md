# PQC Deprecation Lint — RSA/ECC after 2030

Dates every quantum-vulnerable algorithm in your code against the NIST IR 8547 clock: deprecated after 2030-12-31, disallowed after 2035-12-31.

## Install

```
npx @readystack/pqc-deprecation-lint file
```

Node 18+. The same 17 rules as the VS Code extension, from a terminal or CI.

## Free

- Check the file open in the editor and see every quantum-vulnerable algorithm in it, with line numbers and each one dated against the NIST IR 8547 clock for a date you choose
- `--rules` lists every rule

## With a licence ($29 once)

- Sweep the whole workspace in one pass and write a dated migration report file you keep — the artifact for a customer security questionnaire, a migration ticket, or next quarter's diff

```
@readystack/pqc-deprecation-lint --dir ./templates --report html --out report.html
```

A security consultant doing the same cryptographic inventory by hand bills $150-$250 an hour, and the first pass over one repository is a day

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "pqc-deprecation-lint": { "command": "npx", "args": ["-y", "@readystack/pqc-deprecation-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence; the full sweep is free for 7 days). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: PQC Deprecation Lint — RSA/ECC after 2030
  run: npx -y @readystack/pqc-deprecation-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/pqc-deprecation-lint --dir /work --ci`)

Try the full run free for 7 days — no key needed. Then one licence, 7-day refund, no questions. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_Q0a5F9WB3Ub2fTRsFv8TePDwMQjmT1GtVgVGl3H6oee)


<!-- pqc deprecation lint -->

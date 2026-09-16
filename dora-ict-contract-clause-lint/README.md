# DORA Art. 30 ICT Contract Clause Lint

Twenty-two checks over the ICT vendor contracts in your repository - every missing Article 30 clause named, with the wording to paste in.

## Install

```
npx @readystack/dora-ict-contract-clause-lint file
```

Node 18+. The same 22 rules as the VS Code extension, from a terminal or CI.

## Free

- Lint one open ICT vendor contract to the end: every missing DORA Article 30 clause named, with the article reference and the wording to paste in.
- `--rules` lists every rule

## With a licence ($29 once)

- One pass over every contract in the repository plus an exported per-vendor, per-clause evidence table for the register of information and the Q4 audit file.

```
@readystack/dora-ict-contract-clause-lint --dir ./templates --report html --out report.html
```

Outside counsel reading one ICT contract against DORA Article 30 takes two to four hours at roughly EUR 300 an hour for EU financial-regulatory work.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "dora-ict-contract-clause-lint": { "command": "npx", "args": ["-y", "@readystack/dora-ict-contract-clause-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence; the full sweep is free for 7 days). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: DORA Art. 30 ICT Contract Clause Lint
  run: npx -y @readystack/dora-ict-contract-clause-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/dora-ict-contract-clause-lint --dir /work --ci`)

Try the full run free for 7 days — no key needed. Then one licence, 7-day refund, no questions. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_PyS5jRrYO7Qg2eYCctURo3heBw7Z5sPLx4UrE49Ms6L)


<!-- dora ict contract clause lint -->

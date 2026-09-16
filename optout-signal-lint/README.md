# Opt-Out Signal Lint for US State Privacy Laws

Finds the ad and analytics code that keeps firing after a visitor’s browser has already sent Global Privacy Control.

## Install

```
npx @readystack/optout-signal-lint file
```

Node 18+. The same 20 rules as the VS Code extension, from a terminal or CI.

## Free

- Audits the file you have open — every line against all 20 rules, no key, no limit, no sign-up.
- `--rules` lists every rule

## With a licence ($29 once)

- Sweeps the whole workspace, writes the finding list to CSV, JSON or HTML, and returns a CI exit code so the same leak cannot merge twice.

```
@readystack/optout-signal-lint --dir ./templates --report html --out report.html
```

Osano, the nearest hosted consent platform, starts at $199/month.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "optout-signal-lint": { "command": "npx", "args": ["-y", "@readystack/optout-signal-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence; the full sweep is free for 7 days). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: Opt-Out Signal Lint for US State Privacy Laws
  run: npx -y @readystack/optout-signal-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/optout-signal-lint --dir /work --ci`)

Try the full run free for 7 days — no key needed. Then one licence, 7-day refund, no questions. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_gj151VTqWFpXoYSJLn1MtTGUJrDV3N8bEeFLH4cORhY)


<!-- global privacy control -->

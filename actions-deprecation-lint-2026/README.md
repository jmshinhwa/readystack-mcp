# GitHub Actions Deprecation Lint: the 2026 runner and action EOL dates

Node 20 is removed from GitHub-hosted runners on 2026-09-23 and ubuntu-22.04 deprecation opens 2026-09-17. This checks a workflow file against 25 dated GitHub shutdowns and names the date each line stops running.

## Install

```
npx @readystack/actions-deprecation-lint-2026 file
```

Node 18+. The same 25 rules as the VS Code extension, from a terminal or CI.

## Free

- Audit the workflow file you have open against all 25 dated rules - every line, every shutdown date, no key asked.
- `--rules` lists every rule

## With a licence ($29 once)

- Scan every workflow in the repository at once, export the report, fail CI on a finding, re-check on save, and add your own rules.

```
@readystack/actions-deprecation-lint-2026 --dir ./templates --report html --out report.html
```

A freelance DevOps engineer bills about $100/hour in 2026 (goLance 2026 rate guide, range $100-165 for experienced contractors); one blocked release morning costs more than this licence.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "actions-deprecation-lint-2026": { "command": "npx", "args": ["-y", "@readystack/actions-deprecation-lint-2026", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: GitHub Actions Deprecation Lint: the 2026 runner and action EOL dates
  run: npx -y @readystack/actions-deprecation-lint-2026 --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/actions-deprecation-lint-2026 --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_FgqChyU4dcdTz5VWg1S6cM0Taaa73QIq6oV5K0CFWfa)


<!-- actions deprecation lint 2026 -->

# Security Headers Lint - CSP and Dead Headers

Reads security headers and CSP line by line in your config file and names the lines that silently do nothing: retired headers, keywords missing their quotes, directives the browser throws away.

## Install

```
npx @readystack/security-headers-csp-lint file
```

Node 18+. The same 28 rules as the VS Code extension, from a terminal or CI.

## Free

- Check the open config against all 28 rules - every finding shown, nothing withheld; Check only the lines you highlight; See every rule and what each retired header or dropped directive actually does; Reopen the last report
- `--rules` lists every rule

## With a licence ($29 once)

- Scan every config file in the workspace; Export the report as CSV, JSON or HTML; CI output that fails the build on errors; Add your own house policy rules; Re-check automatically on every save; Apply the safe fixes for you

```
@readystack/security-headers-csp-lint --dir ./templates --report html --out report.html
```

Application security consultants doing secure code review bill roughly $120 to $275 an hour, and a security-header and CSP review is a one-to-two hour job per site.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "security-headers-csp-lint": { "command": "npx", "args": ["-y", "@readystack/security-headers-csp-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: Security Headers Lint - CSP and Dead Headers
  run: npx -y @readystack/security-headers-csp-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/security-headers-csp-lint --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_DxnwX3BvMThBo4369WHczw3OVdSlhjnkHsoJb0ZEGWd)


<!-- security headers lint -->

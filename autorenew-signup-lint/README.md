# Auto-Renewal Signup Lint (California ARL)

Sixteen statutory checks on the signup page AB 2863 rewrote, in your editor and in the browser

## Install

```
npx @readystack/autorenew-signup-lint file
```

Node 18+. The same 16 rules as the VS Code extension, from a terminal or CI.

## Free

- Check the signup or pricing page open in the editor against all 16 rules, free and unlimited, plus the same engine free in the browser.
- `--rules` lists every rule

## With a licence ($29 once)

- Sweep every matching page in the workspace and write one dated report file into the folder, yours to keep and attach to a review.

```
@readystack/autorenew-signup-lint --dir ./templates --report html --out report.html
```

An hour of US outside counsel reviewing one signup flow is commonly quoted at $300-$500.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "autorenew-signup-lint": { "command": "npx", "args": ["-y", "@readystack/autorenew-signup-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: Auto-Renewal Signup Lint (California ARL)
  run: npx -y @readystack/autorenew-signup-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/autorenew-signup-lint --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_ysb3yWUhknvn2fWoPwchsZqFfbA3X5hijEY2x1jBBhw)


<!-- california auto renewal signup lint -->

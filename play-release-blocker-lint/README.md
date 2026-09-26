# Google Play Release Blocker Lint - target API 36, Billing 8, 16 KB

Finds the lines that make Google Play reject your release - target API below 36, Billing Library below 8, 4 KB-only native libs - and prints the date each gate closed.

## Install

```
npx @readystack/play-release-blocker-lint file
```

Node 18+. The same 31 rules as the VS Code extension, from a terminal or CI.

## Free

- Full check of the file you have open - every rule, every line, with the gate date and the fix; Reopen the last report without re-running the scan; See every Play gate rule, its severity and its deadline
- `--rules` lists every rule

## With a licence ($29 once)

- Every module, flavour and manifest in the repo at once; Machine-readable output your CI can fail on; A dated release-readiness report you can hand to a client or a lead; Re-checks on every save while you migrate

```
@readystack/play-release-blocker-lint --dir ./templates --report html --out report.html
```

Upwork publishes a $25/hr median for Android developers (typical range $15-$35); one rejected release burns more than that in rebuild-and-resubmit time.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "play-release-blocker-lint": { "command": "npx", "args": ["-y", "@readystack/play-release-blocker-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: Google Play Release Blocker Lint - target API 36, Billing 8, 16 KB
  run: npx -y @readystack/play-release-blocker-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/play-release-blocker-lint --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_gyOsuR4TciVB1eezarZh5whJXfxrUOu4SDZCZ2hu1dw)


<!-- google play target api 36 -->

# EAA Form Lint: WCAG 2.2 AA for HTML

Names every WCAG 2.2 AA form failure on its line, with the criterion and the fix

## Install

```
npx @readystack/eaa-form-lint-wcag22 file
```

Node 18+. The same 18 rules as the VS Code extension, from a terminal or CI.

## Free

- Lints the HTML, Vue or Svelte file you have open with all 18 rules and names every WCAG 2.2 AA form failure on its line, with the success-criterion number and the one-line fix.
- `--rules` lists every rule

## With a licence ($29 once)

- Scans every template in the workspace in one pass and writes a dated conformance evidence file you keep - one row per finding, per file, mapped to its WCAG 2.2 criterion.

```
@readystack/eaa-form-lint-wcag22 --dir ./templates --report html --out report.html
```

A WCAG audit from an accessibility vendor starts around $2,500 for one signup flow

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "eaa-form-lint-wcag22": { "command": "npx", "args": ["-y", "@readystack/eaa-form-lint-wcag22", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: EAA Form Lint: WCAG 2.2 AA for HTML
  run: npx -y @readystack/eaa-form-lint-wcag22 --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/eaa-form-lint-wcag22 --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_O5AMXCnn3ZETWE939bA4zjzmM0KqLt9Yp76Xm2x1Pa1)


<!-- eaa form lint wcag22 -->

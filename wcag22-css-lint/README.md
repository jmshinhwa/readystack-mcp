# WCAG 2.2 CSS Lint - Focus & Target Size

Reads your stylesheet and names the success criterion each rule breaks, including the three WCAG 2.2 added that WCAG 2.1 linters never learned.

## Install

```
npx @readystack/wcag22-css-lint file
```

Node 18+. The same 14 rules as the VS Code extension, from a terminal or CI.

## Free

- Lint the stylesheet you have open against all 14 rules, with the success criterion number, the failing line and the fix on every finding.
- `--rules` lists every rule

## With a licence ($29 once)

- Scan every stylesheet in the workspace in one pass and export the findings as a dated criterion-by-criterion evidence table (Markdown + CSV) you keep and attach to your accessibility statement.

```
@readystack/wcag22-css-lint --dir ./templates --report html --out report.html
```

An accessibility consultant reviewing one stylesheet by hand bills a $150-$250 hour; a full third-party WCAG audit of a site is quoted in the thousands.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "wcag22-css-lint": { "command": "npx", "args": ["-y", "@readystack/wcag22-css-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: WCAG 2.2 CSS Lint - Focus & Target Size
  run: npx -y @readystack/wcag22-css-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/wcag22-css-lint --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_gYGJTycG04gELmMeEpKE2BMsam4llOPlJb69i33u33l)


<!-- wcag22 css lint -->

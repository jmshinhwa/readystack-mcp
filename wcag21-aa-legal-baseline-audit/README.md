# WCAG 2.1 AA Legal Baseline Audit for templates

Audits HTML, JSX, Vue, Twig, Blade, ERB and Razor markup against the 24 WCAG 2.1 Level AA checks that 28 CFR 35.200 and EN 301 549 actually name - not WCAG 2.2.

## Install

```
npx @readystack/wcag21-aa-legal-baseline-audit file
```

Node 18+. The same 24 rules as the VS Code extension, from a terminal or CI.

## Free

- Audits the open template and names the WCAG 2.1 criterion and level for every finding; Audits only the lines you select, keeping the real line numbers; Prints the whole rule sheet - all 24 checks and the criterion each maps to
- `--rules` lists every rule

## With a licence ($29 once)

- Audits every template in the workspace, not the one file you have open; Exports the findings as CSV, JSON or HTML; Applies the mechanical fixes in place; Re-audits automatically on every save

```
@readystack/wcag21-aa-legal-baseline-audit --dir ./templates --report html --out report.html
```

A consultancy WCAG audit is $100-$250 per page (Accessible.org published pricing, 2026); this reads every template in the repository for $29 once.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "wcag21-aa-legal-baseline-audit": { "command": "npx", "args": ["-y", "@readystack/wcag21-aa-legal-baseline-audit", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: WCAG 2.1 AA Legal Baseline Audit for templates
  run: npx -y @readystack/wcag21-aa-legal-baseline-audit --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/wcag21-aa-legal-baseline-audit --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_RArnwX2pmZk48V2VCw2Ep19h2Nnf5FgaiN4oI3Y2nZu)


<!-- wcag 2 1 aa audit ada title ii en 301 549 -->

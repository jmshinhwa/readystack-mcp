# VSIX Publish Lint

Find the package.json lines that stop vsce before you run the release build

## Install

```
npx @readystack/vsix-publish-lint file
```

Node 18+. The same 16 rules as the VS Code extension, from a terminal or CI.

## Free

- Lints the extension manifest you have open against all 16 rules and names, line by line, the exact field to change
- `--rules` lists every rule

## With a licence ($29 once)

- Lints every extension manifest in the workspace in one pass and writes the result out as a JSON or SARIF file you keep and run in CI

```
@readystack/vsix-publish-lint --dir ./templates --report html --out report.html
```

One hour of specialised freelance developer time runs $75-$150 on Upwork's own 2026 rate guide; a rejected publish usually costs more than one.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "vsix-publish-lint": { "command": "npx", "args": ["-y", "@readystack/vsix-publish-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: VSIX Publish Lint
  run: npx -y @readystack/vsix-publish-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/vsix-publish-lint --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_0qIqdKq149OPf1mvGZKukzSvyH1nK9fHwub4l4P27pr)


<!-- vsix publish lint -->

# Model Card Lint - EU GPAI (AI Act Art. 53)

Lints a Hugging Face model card against the Hub metadata spec and the EU AI Act general-purpose AI documentation duties, line by line.

## Install

```
npx @readystack/model-card-lint-gpai file
```

Node 18+. The same 28 rules as the VS Code extension, from a terminal or CI.

## Free

- Lint the model card you have open against all 28 rules, as often as you like - line number, rule id, the article it comes from, and the line to write instead. Runs locally, no key, no upload.
- `--rules` lists every rule

## With a licence ($29 once)

- Lint every model card in the repository in one pass and export the dated audit as a file you keep: Markdown for the reviewer, JSON a CI step can fail on.

```
@readystack/model-card-lint-gpai --dir ./templates --report html --out report.html
```

An hour of an EU AI Act compliance consultant starts near $200; the Act's own ceiling for a GPAI provider is EUR 15,000,000 or 3% of worldwide annual turnover (Art. 101).

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "model-card-lint-gpai": { "command": "npx", "args": ["-y", "@readystack/model-card-lint-gpai", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: Model Card Lint - EU GPAI (AI Act Art. 53)
  run: npx -y @readystack/model-card-lint-gpai --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/model-card-lint-gpai --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_mHiMKq8aRodhSAoK7NzNGXWSa5Nxn3sBnksN74QXeId)


<!-- model card lint gpai -->

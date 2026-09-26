# AI Model Retirement Lint

Finds the LLM model IDs pinned in your code that vendors have already switched off, or have dated to switch off, with the replacement and the date.

## Install

```
npx @readystack/ai-model-retirement-lint file
```

Node 18+. The same 33 rules as the VS Code extension, from a terminal or CI.

## Free

- Checks the file you have open against all 33 rules and names every retired or expiring model ID, its date and the vendor's replacement - no key, no limit, no watermark.
- `--rules` lists every rule

## With a licence ($29 once)

- Scans every file in the repository, emits CI output that fails the build before a dead model ID can merge, and applies the vendor's replacement in place.

```
@readystack/ai-model-retirement-lint --dir ./templates --report html --out report.html
```

OpenAI removes 12 model IDs from the API in one sweep on 2026-10-23; Anthropic gives 60 days notice before a retirement.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "ai-model-retirement-lint": { "command": "npx", "args": ["-y", "@readystack/ai-model-retirement-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: AI Model Retirement Lint
  run: npx -y @readystack/ai-model-retirement-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/ai-model-retirement-lint --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_EOiE7ckv1WZujsc6UOfnGhc0lxBYyaPS8uZLl2Fo9Ap)


<!-- ai model retirement lint -->

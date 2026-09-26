# DORA Register of Information Lint

24 checks on the register CSV before it reaches the supervisor — LEI check digits, ISO dates and codes, references that resolve

## Install

```
npx @readystack/dora-register-lint file
```

Node 18+. The same 24 rules as the VS Code extension, from a terminal or CI.

## Free

- Check the register CSV open in your editor - every row, all 24 checks, findings in the Problems panel and a written summary in the output channel, no key and no account
- `--rules` lists every rule

## With a licence ($29 once)

- Sweep every register CSV in the workspace and write one dated report file (doraRegister-report.md) you can attach to the audit trail

```
@readystack/dora-register-lint --dir ./templates --report html --out report.html
```

One hour of the compliance analyst who would otherwise re-check the file by hand costs more than the licence; a manual pass over an 800-row register is 24 x 800 = 19,200 check-row comparisons.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "dora-register-lint": { "command": "npx", "args": ["-y", "@readystack/dora-register-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: DORA Register of Information Lint
  run: npx -y @readystack/dora-register-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/dora-register-lint --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_4WZMkiJUxjGBBEqJo7hbkQ7REYH8kJIOWwGoJ29agpN)


<!-- dora register lint -->

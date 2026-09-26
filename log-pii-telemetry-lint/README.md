# PII-in-Logs Lint (console.log(req.body))

22 rules that name the lines where a Node or TypeScript service writes personal data into logs, crash reports and analytics — with the article it touches and the one-line fix.

## Install

```
npx @readystack/log-pii-telemetry-lint file
```

Node 18+. The same 22 rules as the VS Code extension, from a terminal or CI.

## Free

- Names every line in the file you have open that writes personal data into a log, a crash report or an analytics call, with the rule, the article it touches and the one-line fix — enough to clean that file and stop.
- `--rules` lists every rule

## With a licence ($29 once)

- Runs the same 22 rules across every .js/.ts file in the workspace and writes the findings out as a report file you keep for CI, the ticket or the auditor.

```
@readystack/log-pii-telemetry-lint --dir ./templates --report html --out report.html
```

GitHub Advanced Security lists at $49 per active committer per month ($30 Code Security + $19 Secret Protection) and looks for secrets, not for a customer's name travelling in a log line.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "log-pii-telemetry-lint": { "command": "npx", "args": ["-y", "@readystack/log-pii-telemetry-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: PII-in-Logs Lint (console.log(req.body))
  run: npx -y @readystack/log-pii-telemetry-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/log-pii-telemetry-lint --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_NLG690BJU22qAXNWaQROOaDLw4Mg1DA9xifr10uIElw)


<!-- log pii telemetry lint -->

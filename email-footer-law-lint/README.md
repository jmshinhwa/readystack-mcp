# Email Footer Law Lint

Fourteen checks on an HTML email footer: CAN-SPAM postal address and 10-business-day opt-out, CASL's 60-day window, and German 5 DDG, the statute that replaced 5 TMG on 2024-05-14.

## Install

```
npx @readystack/email-footer-law-lint file
```

Node 18+. The same 14 rules as the VS Code extension, from a terminal or CI.

## Free

- Check the email template open in your editor against all 14 footer-law rules, every finding carrying its line, its statute and its fix
- `--rules` lists every rule

## With a licence ($29 once)

- Sweep every template in the workspace and write one dated, citable audit report file you can hand to a client or to counsel

```
@readystack/email-footer-law-lint --dir ./templates --report html --out report.html
```

Outside counsel reads one email footer against CAN-SPAM, CASL and 5 DDG at about $300 an hour, and reads it once.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "email-footer-law-lint": { "command": "npx", "args": ["-y", "@readystack/email-footer-law-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: Email Footer Law Lint
  run: npx -y @readystack/email-footer-law-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/email-footer-law-lint --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_UpcPQkomm2d1N52PaYHHfPjdB89okIRPLaTa70CzAj0)


<!-- email footer law lint -->

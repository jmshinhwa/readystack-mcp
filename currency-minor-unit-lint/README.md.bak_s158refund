# Currency Minor Unit Lint

Finds the money lines that send the wrong amount to a payment API: the x100 that charges 100x in JPY, the toFixed(2) that truncates KWD, and the currency codes that stopped being legal tender.

## Install

```
npx @readystack/currency-minor-unit-lint file
```

Node 18+. The same 24 rules as the VS Code extension, from a terminal or CI.

## Free

- Checks the file you have open against all 24 rules and names every wrong amount, its currency, its ISO 4217 exponent and the date a code changed - no key, no limit, no watermark.
- `--rules` lists every rule

## With a licence ($29 once)

- Scans every file in the repository, fails a CI build before a wrong amount can merge, exports the findings as CSV, JSON or HTML, and rewrites the retired currency codes in place.

```
@readystack/currency-minor-unit-lint --dir ./templates --report html --out report.html
```

Payment processors publish a $15.00 fee for every dispute received, and it is not returned when you lose the dispute.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "currency-minor-unit-lint": { "command": "npx", "args": ["-y", "@readystack/currency-minor-unit-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence; the full sweep is free for 7 days). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: Currency Minor Unit Lint
  run: npx -y @readystack/currency-minor-unit-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/currency-minor-unit-lint --dir /work --ci`)

Try the full run free for 7 days — no key needed. Then one licence, 7-day refund, no questions. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_acLdPf1V4wK36zA20Zdz5ARBivvJMJv1kJ9JI2lqb50)


<!-- currency minor unit lint -->

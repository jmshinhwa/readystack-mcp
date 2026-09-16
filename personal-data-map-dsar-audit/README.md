# Personal Data Map: find every column a GDPR subject access request has to reach

Reads a migration, Prisma schema, Django model or TypeORM entity and marks every column a subject access request has to reach - with the GDPR article each finding hangs on. 13 rules, line numbers, no account.

## Install

```
npx @readystack/personal-data-map-dsar-audit file
```

Node 18+. The same 13 rules as the VS Code extension, from a terminal or CI.

## Free

- Run all 13 GDPR schema rules over the migration or model you have open - every line, every article, no account and no key asked.
- `--rules` lists every rule

## With a licence ($29 once)

- Map every migration and model in the repository at once, export the map as CSV, JSON or HTML for the Art. 30 record, and write JSON your CI can fail on.

```
@readystack/personal-data-map-dsar-audit --dir ./templates --report html --out report.html
```

An independent EU privacy consultant bills EUR 100-200/hour (market average about EUR 150) and one manual DSAR averages about $1,524 in staff time across 8-12 hours.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "personal-data-map-dsar-audit": { "command": "npx", "args": ["-y", "@readystack/personal-data-map-dsar-audit", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence; the full sweep is free for 7 days). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: Personal Data Map: find every column a GDPR subject access request has to reach
  run: npx -y @readystack/personal-data-map-dsar-audit --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/personal-data-map-dsar-audit --dir /work --ci`)

Try the full run free for 7 days — no key needed. Then one licence, 7-day refund, no questions. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_BXPHG1fr7NIyCwKd6UwVuUit0HVpNLllIqENN46kmIz)


<!-- personal data map dsar audit -->

# WordPress Privacy Lint (GDPR / DSGVO)

Finds the 12 author-side privacy duties your plugin PHP breaks, with the article and the fix on every line.

## Install

```
npx @readystack/wordpress-privacy-lint file
```

Node 18+. The same 12 rules as the VS Code extension, from a terminal or CI.

## Free

- Audits the PHP file you have open against all 12 author-side GDPR/DSGVO rules and names the article and the fix for every hit.
- `--rules` lists every rule

## With a licence ($29 once)

- Scans every PHP file in the whole plugin in one run and writes a dated audit report you keep (Markdown and JSON) for the WordPress.org review reply and your Art. 30 records.

```
@readystack/wordpress-privacy-lint --dir ./templates --report html --out report.html
```

A DSGVO code review by a German IT-law firm is commonly billed at EUR 200 per hour, and a Google Fonts Abmahnung letter is typically settled at EUR 100 plus fees.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "wordpress-privacy-lint": { "command": "npx", "args": ["-y", "@readystack/wordpress-privacy-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence; the full sweep is free for 7 days). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: WordPress Privacy Lint (GDPR / DSGVO)
  run: npx -y @readystack/wordpress-privacy-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/wordpress-privacy-lint --dir /work --ci`)

Try the full run free for 7 days — no key needed. Then one licence, 7-day refund, no questions. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_sZ2Bgyx7lAEhKmhzceABGE3rRlKWXaJxUrjPm48Q1KV)


<!-- wordpress privacy lint -->

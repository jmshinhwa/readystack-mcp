# GPSR Listing Lint

Audits a product feed row by row against Article 19 of the EU General Product Safety Regulation

## Install

```
npx @readystack/gpsr-listing-lint file
```

Node 18+. The same 12 rules as the VS Code extension, from a terminal or CI.

## Free

- Open any product feed file and see every listing row that is missing a GPSR Article 19 field, with its line number and the exact article it fails — no key, nothing uploaded.
- `--rules` lists every rule

## With a licence ($29 once)

- Export a dated evidence pack for the whole workspace catalogue — every feed file, every failing row, per-rule counts — as CSV and Markdown you can hand to a marketplace, importer or auditor.

```
@readystack/gpsr-listing-lint --dir ./templates --report html --out report.html
```

An EU Responsible Person / authorised-representative service is sold as a monthly subscription, per brand; hand-checking a feed at ten seconds a row is about fourteen hours for five thousand rows. This is $29 once.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "gpsr-listing-lint": { "command": "npx", "args": ["-y", "@readystack/gpsr-listing-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence; the full sweep is free for 7 days). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: GPSR Listing Lint
  run: npx -y @readystack/gpsr-listing-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/gpsr-listing-lint --dir /work --ci`)

Try the full run free for 7 days — no key needed. Then one licence, 7-day refund, no questions. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_MeEOXqXAf3FoF5aXVJjeeyaoJJNIODsmsm5CK0skgvG)


<!-- gpsr listing lint -->

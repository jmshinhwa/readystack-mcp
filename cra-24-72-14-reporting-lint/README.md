# CRA 24/72/14 Reporting Lint (Article 14)

Reads your SECURITY.md against the EU Cyber Resilience Act reporting clock that started on 11 September 2026 — 24 hours, 72 hours, 14 days, to ENISA and your coordinating CSIRT.

## Install

```
npx @readystack/cra-24-72-14-reporting-lint file.md
```

Node 18+. The same 18 rules as the VS Code extension, from a terminal or CI.

## Free

- Checks the Markdown file you have open against all 18 rules, offline, with the article and the replacement line for every finding — no watermark, no counter, nothing withheld.
- `--rules` lists every rule

## With a licence ($29 once)

- Sweeps every Markdown file in the workspace in one pass, works out which checks are answered nowhere in the repository rather than merely missing from one file, and writes one dated CRA-24-72-14-READINESS.md to hand to an auditor.

```
@readystack/cra-24-72-14-reporting-lint --dir ./templates --report html --out report.html
```

One hour of EU product-compliance consulting runs $150-250, and a first documentation review is rarely one hour.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "cra-24-72-14-reporting-lint": { "command": "npx", "args": ["-y", "@readystack/cra-24-72-14-reporting-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: CRA 24/72/14 Reporting Lint (Article 14)
  run: npx -y @readystack/cra-24-72-14-reporting-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/cra-24-72-14-reporting-lint --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_zmN08yKAf6Qz5WMiSQO9V9MxIRQN87VQEfurn03M3KT)


<!-- cra 24 72 14 reporting lint -->

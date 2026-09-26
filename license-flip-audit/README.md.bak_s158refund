# License Flip Audit - BUSL/SSPL/AGPL in your deps

Finds the dependencies whose licence changed under you - Terraform 1.6+ BUSL, Redis 7.4+ SSPL, Bitnami's August 2025 move, Elastic 7.11 - and names the exact version where each flip happened.

## Install

```
npx @readystack/license-flip-audit file
```

Node 18+. The same 30 rules as the VS Code extension, from a terminal or CI.

## Free

- Checks the manifest you have open end to end - every line, all 30 recorded flips, full findings, no watermark and no trial.
- `--rules` lists every rule

## With a licence ($29 once)

- Scans every manifest in the workspace, exports the CSV/JSON/HTML report a security review asks for, re-checks on every save, and writes a JSON file CI can fail a pull request on.

```
@readystack/license-flip-audit --dir ./templates --report html --out report.html
```

The Bitnami flip alone pushed teams onto a Bitnami Secure subscription reported at $50,000-$72,000 a year.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "license-flip-audit": { "command": "npx", "args": ["-y", "@readystack/license-flip-audit", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence; the full sweep is free for 7 days). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: License Flip Audit - BUSL/SSPL/AGPL in your deps
  run: npx -y @readystack/license-flip-audit --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/license-flip-audit --dir /work --ci`)

Try the full run free for 7 days — no key needed. Then one licence, 7-day refund, no questions. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_sFzJiUXy6pSbEx0SFN1aIg7vRguyRc32MpDnb1iCHPe)


<!-- license flip audit -->

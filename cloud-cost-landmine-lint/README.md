# Cloud Cost Landmine Lint for Terraform, CloudFormation and Kubernetes

Names every line in the file you have open that starts a recurring cloud charge, with the published us-east-1 price and the date it changes by itself.

## Install

```
npx @readystack/cloud-cost-landmine-lint file
```

Node 18+. The same 27 rules as the VS Code extension, from a terminal or CI.

## Free

- Checks the file you have open against all 27 rules and names every line that starts a standing charge, with its published us-east-1 unit price and the date it changes on its own - no key, no limit, no watermark.
- `--rules` lists every rule

## With a licence ($29 once)

- Scans every file in the repository at once, exports the findings as CSV, JSON or HTML for a budget review, and prints machine output that exits non-zero so a pipeline can stop a merge that adds a standing charge.

```
@readystack/cloud-cost-landmine-lint --dir ./templates --report html --out report.html
```

Amazon's own published price for the same untouched cluster after the date passes: $0.60 per cluster-hour instead of $0.10, which is $365 more every month.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "cloud-cost-landmine-lint": { "command": "npx", "args": ["-y", "@readystack/cloud-cost-landmine-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: Cloud Cost Landmine Lint for Terraform, CloudFormation and Kubernetes
  run: npx -y @readystack/cloud-cost-landmine-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/cloud-cost-landmine-lint --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_Ia8TdkkJhasNMqHS8HGMSeb7xmNWI6NKp02Mt3Fj1JG)


<!-- cloud cost landmine lint -->

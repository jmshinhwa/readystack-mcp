# TLS Cert Lifetime Lint - SC-081v3 renewal check

Finds the 12 settings that break when public TLS certificates fall to 100 days on 2027-03-15: openssl -days, Terraform, cert-manager, late expiry alerts, HPKP, TLS 1.0/1.1, SHA-1, RSA-1024.

## Install

```
npx @readystack/tls-cert-lifetime-lint file
```

Node 18+. The same 12 rules as the VS Code extension, from a terminal or CI.

## Free

- Names the exact date each setting stops working - 2026-03-15 (200 days), 2027-03-15 (100 days), 2029-03-15 (47 days); Reads openssl commands, Terraform, cert-manager YAML, nginx and Apache config, Go tls.Config and Prometheus alert rules; Shows every finding in the open file with its line number - nothing is held back or blurred; Catches runbooks and comments that still quote the retired 397, 398 or 825-day maximum; Separates what is already broken today from what breaks on the next milestone
- `--rules` lists every rule

## With a licence ($29 once)

- The whole repository, not one open file; Take the findings away as CSV, JSON or HTML; CI JSON a pipeline can fail on

```
@readystack/tls-cert-lifetime-lint --dir ./templates --report html --out report.html
```

A certificate lifecycle management platform starts at $50,000-$100,000 a year plus $1-$5 per certificate (Keyfactor Command, 2026 vendor pricing).

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "tls-cert-lifetime-lint": { "command": "npx", "args": ["-y", "@readystack/tls-cert-lifetime-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: TLS Cert Lifetime Lint - SC-081v3 renewal check
  run: npx -y @readystack/tls-cert-lifetime-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/tls-cert-lifetime-lint --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_SnmEdHDa8OjzORnIjOry1XW7LZozu9qDBYIIc1eBSB5)


<!-- tls certificate lifetime -->

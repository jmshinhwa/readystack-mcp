# Firmware Release Gate for sdkconfig and prj.conf

Finds the build-config lines that ship an ESP-IDF or Zephyr device with secure boot off, a debug port open, unsigned images or plaintext OTA.

## Install

```
npx @readystack/firmware-release-gate file
```

Node 18+. The same 18 rules as the VS Code extension, from a terminal or CI.

## Free

- Audit the config file you have open, top to bottom; List the rules that ship inside; Re-open the last audit report
- `--rules` lists every rule

## With a licence ($29 once)

- Audit every config in the workspace; Export the audit report as CSV, JSON or HTML; Machine-readable JSON for CI

```
@readystack/firmware-release-gate --dir ./templates --report html --out report.html
```

An outside firmware-only security review starts around $6,000 and a full IoT device assessment runs $10,000 to $50,000; this is the config pass you run before you pay for one.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "firmware-release-gate": { "command": "npx", "args": ["-y", "@readystack/firmware-release-gate", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: Firmware Release Gate for sdkconfig and prj.conf
  run: npx -y @readystack/firmware-release-gate --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/firmware-release-gate --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_cmmWDH5sYqYlHlEAy4aCkF8gPdT40c3FhYupJ1VFP22)


<!-- esp-idf sdkconfig secure boot -->

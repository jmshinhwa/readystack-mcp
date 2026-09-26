# Base Image EOL Lint - Dockerfile and CI end-of-life check

Marks every base image in your Dockerfiles, compose files and CI workflows whose security patches have already stopped - or stop before 13 November 2026 - and prints the tag that replaces it.

## Install

```
npx @readystack/base-image-eol-lint file
```

Node 18+. The same 21 rules as the VS Code extension, from a terminal or CI.

## Free

- Checks the file you have open against all 21 rules and shows every out-of-support image with the tag that replaces it and how long it has been unpatched - no key, no limit, no watermark.
- `--rules` lists every rule

## With a licence ($29 once)

- Scans every Dockerfile, compose file and workflow in the repository at once, writes a dated CSV/JSON/HTML report, and prints machine-readable output so CI fails the build before an unpatched base image ships.

```
@readystack/base-image-eol-lint --dir ./templates --report html --out report.html
```

Snyk's Team tier is $25 per contributing developer per month.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "base-image-eol-lint": { "command": "npx", "args": ["-y", "@readystack/base-image-eol-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: Base Image EOL Lint - Dockerfile and CI end-of-life check
  run: npx -y @readystack/base-image-eol-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/base-image-eol-lint --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_brZKgBkvnYrEIMElB5Ynt5gGEnqmTjvx9r9ZX3ljztR)


<!-- dockerfile base image end of life -->

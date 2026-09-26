# Kubernetes Removed API Lint

15 checks for the apiVersions kubectl no longer serves, on the manifest open in your editor

## Install

```
npx @readystack/k8s-removed-api-lint file
```

Node 18+. The same 15 rules as the VS Code extension, from a terminal or CI.

## Free

- Check the manifest open in the editor against all 15 rules and get the removal release and the replacement apiVersion for every hit - a finished answer for that file, no key
- `--rules` lists every rule

## With a licence ($29 once)

- Sweep every manifest in the workspace and write one dated migration report ordered by removal version - the same 15 rules at repo scope

```
@readystack/k8s-removed-api-lint --dir ./templates --report html --out report.html
```

A freelance Kubernetes consultant bills about 120 US dollars an hour, and reading one chart repo for beta apiVersions before an upgrade is most of a day

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "k8s-removed-api-lint": { "command": "npx", "args": ["-y", "@readystack/k8s-removed-api-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: Kubernetes Removed API Lint
  run: npx -y @readystack/k8s-removed-api-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/k8s-removed-api-lint --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_KTPvcCTdnbtM5Aee1mJ5vKkTnXi90z2QikiQy1sh8m7)


<!-- k8s removed api lint -->

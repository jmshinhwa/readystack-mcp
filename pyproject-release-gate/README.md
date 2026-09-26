# pyproject.toml Release Gate (PEP 639)

19 date-aware checks on the [project] metadata that decides whether your next release uploads

## Install

```
npx @readystack/pyproject-release-gate file
```

Node 18+. The same 19 rules as the VS Code extension, from a terminal or CI.

## Free

- Every one of the 19 findings for the pyproject.toml open in your editor, with the line number, the spec that moved and the replacement text — nothing withheld, no watermark, no counter
- `--rules` lists every rule

## With a licence ($29 once)

- Sweeping every pyproject.toml in a monorepo in one pass and writing a dated report file you keep in the repo and attach to a pull request

```
@readystack/pyproject-release-gate --dir ./templates --report html --out report.html
```

One hour of a senior Python developer's time costs more than the licence, in any market that publishes to PyPI — and without this the review has to happen by hand at every release.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "pyproject-release-gate": { "command": "npx", "args": ["-y", "@readystack/pyproject-release-gate", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: pyproject.toml Release Gate (PEP 639)
  run: npx -y @readystack/pyproject-release-gate --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/pyproject-release-gate --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_Dwv8rDHzgqaWnEsVKKqSDvaTApy7kMa9XNhx70ttYbL)


<!-- pyproject release gate -->

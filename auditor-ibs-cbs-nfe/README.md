# Auditor IBS/CBS para NF-e — NT 2025.002

A rejeição por falta de IBS/CBS foi suspensa em 31/07/2026: sua NF-e é autorizada mesmo errada. Este auditor lê o XML no editor e aponta o que a SEFAZ deixou passar.

## Install

```
npx @readystack/auditor-ibs-cbs-nfe file
```

Node 18+. The same 11 rules as the VS Code extension, from a terminal or CI.

## Free

- Audita um XML de NF-e inteiro no editor, offline, com as 11 regras da NT 2025.002 e mostra linha, problema e correção.
- `--rules` lists every rule

## With a licence ($29 once)

- Audita todos os XMLs do workspace de uma vez, exporta o laudo em CSV/JSON/HTML e devolve saída JSON para o CI.

```
@readystack/auditor-ibs-cbs-nfe --dir ./templates --report html --out report.html
```

Assinaturas de apoio à Reforma Tributária para times fiscais partem de R$ 147/mês; esta licença é paga uma única vez.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "auditor-ibs-cbs-nfe": { "command": "npx", "args": ["-y", "@readystack/auditor-ibs-cbs-nfe", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: Auditor IBS/CBS para NF-e — NT 2025.002
  run: npx -y @readystack/auditor-ibs-cbs-nfe --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/auditor-ibs-cbs-nfe --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_rSz0yDSxN0wNzfxbbg7AsA7XPlBvfDqRkQ1OC3mWf2r)


<!-- auditor ibs cbs nfe -->

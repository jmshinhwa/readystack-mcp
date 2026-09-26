# インボイス経過措置リンター 2026（80%→70%）

2026年9月30日で80%控除が終わります。10月1日からは50%ではなく70%です（令和8年度税制改正）。請求・仕入コードに残った 0.8 と 0.5、明細ごとの端数処理、T+13桁でない登録番号を、行番号と修正案つきで指摘します。

## Install

```
npx @readystack/jct-transition-lint-2026 file
```

Node 18+. The same 24 rules as the VS Code extension, from a terminal or CI.

## Free

- 請求・仕入の計算コードを1ファイル貼るか開くだけで、24規則すべてを当てて、行番号・深刻度・修正案つきの指摘を全部そのまま出します。件数を隠したり、ぼかしたり、途中で止めたりしません。コードは端末から出ません。
- `--rules` lists every rule

## With a licence ($29 once)

- 1ファイルではなくリポジトリ全体を走査し、指摘一覧を CSV/JSON/HTML に書き出し、保存のたびに再検査し、CI が読む JSON を出します。2026年10月1日以降に 0.8 が戻ってくるのを、プルリクで機械が止めます。

```
@readystack/jct-transition-lint-2026 --dir ./templates --report html --out report.html
```

税理士のスポット相談は1時間5,000〜15,000円、高度な税務判断を伴う相談では10,000〜30,000円が相場です。

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "jct-transition-lint-2026": { "command": "npx", "args": ["-y", "@readystack/jct-transition-lint-2026", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: インボイス経過措置リンター 2026（80%→70%）
  run: npx -y @readystack/jct-transition-lint-2026 --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/jct-transition-lint-2026 --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_akmxSIxDli9uaowwy6ffgNIUozrZ7Qxg6oYFn3rQphD)


<!-- jct transition lint 2026 -->

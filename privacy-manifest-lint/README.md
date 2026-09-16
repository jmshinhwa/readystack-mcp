# Privacy Manifest Lint - xcprivacy & ITMS-91053

Checks PrivacyInfo.xcprivacy and your C#, Dart, JS, Swift and Kotlin source for Apple required-reason APIs, and decodes all 17 reason codes back to the category they belong to.

## Install

```
npx @readystack/privacy-manifest-lint file
```

Node 18+. The same 48 rules as the VS Code extension, from a terminal or CI.

## Free

- Decodes all 17 reason codes back to the category they belong to, with Apple's condition; Flags reason codes Apple never issued - the ones a chatbot invents; Finds required-reason API call sites in C#, Dart, JS/TS, Swift, Obj-C and Kotlin; Flags misspelled manifest keys and category names
- `--rules` lists every rule

## With a licence ($29 once)

- Whole repo, not one open file; Take the report away as CSV, JSON or HTML; CI JSON your pipeline can gate on; Fixes the misspelled keys in place

```
@readystack/privacy-manifest-lint --dir ./templates --report html --out report.html
```

An experienced freelance iOS developer bills $85-145/hour in 2026.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "privacy-manifest-lint": { "command": "npx", "args": ["-y", "@readystack/privacy-manifest-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence; the full sweep is free for 7 days). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: Privacy Manifest Lint - xcprivacy & ITMS-91053
  run: npx -y @readystack/privacy-manifest-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/privacy-manifest-lint --dir /work --ci`)

Try the full run free for 7 days — no key needed. Then one licence, 7-day refund, no questions. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_FqPgaCWDs6XopadWNiuJdDK0t434XmIx9iHsw1X3dFZ)


<!-- privacy manifest lint -->

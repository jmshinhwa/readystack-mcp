# LaTeX Submission Lint: Desk-Reject Check

Seventeen rules on your .tex file: the statements the editorial office looks for, and the source that breaks the publisher's build.

## Install

```
npx @readystack/latex-submission-lint file
```

Node 18+. The same 17 rules as the VS Code extension, from a terminal or CI.

## Free

- Checks the .tex file you have open against all 17 submission rules and writes a line-numbered report of every statement the publisher will look for and cannot find.
- `--rules` lists every rule

## With a licence ($29 once)

- Runs the same 17 rules over every .tex file in the project, follows the include chain of a split manuscript, and exports one submission-readiness report for the whole paper.

```
@readystack/latex-submission-lint --dir ./templates --report html --out report.html
```

Manuscript editing services price per word, from about $0.05, so a 6,000-word paper runs to roughly $300 and a revision cycle takes days.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "latex-submission-lint": { "command": "npx", "args": ["-y", "@readystack/latex-submission-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence; the full sweep is free for 7 days). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: LaTeX Submission Lint: Desk-Reject Check
  run: npx -y @readystack/latex-submission-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/latex-submission-lint --dir /work --ci`)

Try the full run free for 7 days — no key needed. Then one licence, 7-day refund, no questions. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_uLmgCBAZSFSJQ8Yvoose6IUOjSzo0hTMNwRg221VgCt)


<!-- latex submission lint -->

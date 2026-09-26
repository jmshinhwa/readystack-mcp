# AI Crawler Rules - robots.txt Audit for AI Search

Checks robots.txt line by line and says what each AI crawler token actually controls - training, AI-search citation, or user fetch - and which lines silently do nothing.

## Install

```
npx @readystack/robots-txt-ai-crawler-audit file
```

Node 18+. The same 19 rules as the VS Code extension, from a terminal or CI.

## Free

- Check the open robots.txt against every rule - full results, nothing withheld; Check only the lines you highlight; See every rule and what each AI token controls; Reopen the last report
- `--rules` lists every rule

## With a licence ($29 once)

- Scan every robots.txt in the workspace; Export the report as CSV, JSON or HTML; CI output that fails the build on errors; Add your own agency policy tokens; Re-check automatically on every save

```
@readystack/robots-txt-ai-crawler-audit --dir ./templates --report html --out report.html
```

A freelance technical SEO consultant bills roughly $100-150 an hour, and an AI-crawler robots.txt review is a one-to-two hour job.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "robots-txt-ai-crawler-audit": { "command": "npx", "args": ["-y", "@readystack/robots-txt-ai-crawler-audit", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: AI Crawler Rules - robots.txt Audit for AI Search
  run: npx -y @readystack/robots-txt-ai-crawler-audit --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/robots-txt-ai-crawler-audit --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_I8R8AzowzmASHy45ujvewcvtcl4wBBfC2Fe7r3fZwpr)


<!-- ai crawler rules for robots txt -->

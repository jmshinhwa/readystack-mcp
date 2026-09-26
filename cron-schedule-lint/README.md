# Cron Schedule Lint for crontab, Kubernetes CronJob, GitHub Actions, Spring and EventBridge

Names every schedule line in the file you have open that fires at the wrong hour, twice, or never at all - and prints the next three times each one really fires, in the zone that actually applies.

## Install

```
npx @readystack/cron-schedule-lint file
```

Node 18+. The same 29 rules as the VS Code extension, from a terminal or CI.

## Free

- Checks the file you have open against all 29 rules and, for every schedule line, prints the next three instants it really fires at, how many times it fires in a year, and the exact dates when that wall-clock time does not exist or happens twice - no key, no limit, no watermark.
- `--rules` lists every rule

## With a licence ($29 once)

- Merges every schedule in the repository into one calendar instead of the single file you have open, exports it as CSV, JSON or HTML for a change review, and writes machine output a CI step can fail on so a merge cannot add a schedule that never fires.

```
@readystack/cron-schedule-lint --dir ./templates --report html --out report.html
```

Healthchecks.io Business, the ordinary cron monitor, is $20 every month for 100 jobs - $240 a year, forever - and by design it can only tell you after a run was already missed.

## Use from an AI agent (MCP)

Claude Code · Cursor · Windsurf · any MCP client - add to your MCP config:

```json
{ "mcpServers": { "cron-schedule-lint": { "command": "npx", "args": ["-y", "@readystack/cron-schedule-lint", "--mcp"] } } }
```

Tools: `check_text` and `check_file` (free) · `check_dir` (licence). The agent gets every finding with the line number.

## Use in CI

```yaml
- name: Cron Schedule Lint for crontab, Kubernetes CronJob, GitHub Actions, Spring and EventBridge
  run: npx -y @readystack/cron-schedule-lint --dir . --ci
```

(container: `docker run --rm -v "$PWD:/work" getreadystack/cron-schedule-lint --dir /work --ci`)

The folder sweep, reports and CI mode need one licence — one payment, no subscription. Set `READYSTACK_LICENSE=<key>` or run `--license <key>` once.

[Get a licence](https://buy.polar.sh/polar_cl_t0Tavjz6GbjmBsKk04ImLmG6Y3VDIbuP0pht50WAFPX)


<!-- cron schedule lint -->

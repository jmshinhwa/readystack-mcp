# ReadyStack Compliance Lint

Two tools from the `readystack` MCP server:

- `find_checker` - search the checker library by regulation, deadline, file type or platform (any language), e.g. "GDPR privacy notice", "github actions node 20", "XRechnung".
- `run_checker` - run one checker on a file's contents and get every finding with its line, severity, the rule it breaks and the fix.

When the user asks whether a file, policy, config or workflow meets a regulation or a dated platform rule: call `find_checker`, pick the best match, read the file, then call `run_checker` with its contents and file name. Report findings by line with the fix. The checks are deterministic rules; the text is not stored.

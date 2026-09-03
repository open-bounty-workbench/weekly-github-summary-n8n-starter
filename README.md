# GitHub Weekly Summary — n8n Starter

A free preflight workflow for checking the configuration needed to automate a weekly GitHub engineering summary.

It validates the repository identifier, output language, and Slack webhook URL before you connect GitHub or an LLM. Use it as a safe first import when setting up an n8n reporting automation.

## What this starter does

- Runs manually in n8n.
- Validates `owner/repository`, `EN` or `FR`, and an HTTPS Slack webhook URL.
- Produces a ready-to-copy configuration report and next steps.
- Contains no credentials and makes no network requests.

## Five-minute setup

1. Import `weekly-summary-preflight-n8n.json` into n8n.
2. Set `githubRepo`, `language`, and `destinationWebhookUrl` in **Configuration**.
3. Click **Execute Workflow**.
4. Fix any reported configuration error.
5. Move to the complete workflow when the preflight succeeds.

## Complete workflow

The full [Weekly GitHub Narrative Summary for n8n](https://payhip.com/b/mG0zF) adds:

- A Friday 17:00 schedule.
- GitHub GraphQL collection of commits, closed issues, and merged pull requests.
- Claude Sonnet narrative generation based only on fetched activity.
- Slack webhook delivery and an English/French switch.

## License

MIT for the starter files. The complete workflow is sold separately under its product license.

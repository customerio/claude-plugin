# Customer.io plugin for Claude

Official Customer.io plugin for **Claude Code** and **Cowork**: the hosted
**MCP connector** plus **skills** and **slash commands** for Journeys, Data
Pipelines, Design Studio, and SDK setup.

Skills in git are thin routers: the real playbooks live on the MCP server
(`cio_skills_read`) so they update with the product without a plugin release.

## Install

From the Claude plugin directory (once published), or directly:

```
/plugin marketplace add customerio/claude-plugin
/plugin install customerio@customerio
```

## Connect

The plugin bundles the hosted connector (`mcp.customer.io`). The first tool
call opens Customer.io OAuth: pick workspaces plus scopes. The account's home
region is selected after login.

Do not paste a personal MCP URL. Do not add a second Customer.io MCP server.

## Skill

One skill, `customerio`: it connects the MCP server, walks a user with no account through signup, then points the agent to `cio_prime` and the server’s skills.

## Commands

The connector serves these as slash commands once it's connected:

| Command | Does |
| --- | --- |
| `/mcp__customerio__campaign-report` | Metrics + recommendations for an automation |
| `/mcp__customerio__build-segment` | Segment from a plain-English audience description |
| `/mcp__customerio__draft-email` | Design Studio draft with QA review |
| `/mcp__customerio__workspace-health` | Read-only deliverability/pipeline diagnosis |

## Docs

- Setup: https://docs.customer.io/ai/plugins/claude/
- Publishing this repo: [docs/PUBLISH.md](docs/PUBLISH.md)

## License

MIT — see [LICENSE](LICENSE).

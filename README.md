# Customer.io plugin for Claude

Official Customer.io plugin for **Claude Code** and **Cowork**: the hosted
**MCP connector** plus **skills** and **slash commands** for Journeys, Data
Pipelines, Design Studio, and SDK setup.

The skills mirror [customerio/cursor-plugin](https://github.com/customerio/cursor-plugin)
1:1 — that repo is the source of truth for skill content; port changes here
when they land there. Skills in git are thin routers: the real playbooks live
on the MCP server (`cio_skills_read`) so they update with the product without
a plugin release.

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

## Skills

| Skill | Use for | Then read from MCP |
| --- | --- | --- |
| `customerio` | Bootstrap, region, dry-run, routing | `cio_prime` |
| `customerio-journeys` | Automations, profiles, segments, broadcasts, transactional, in-app | `fly-api` |
| `customerio-design-studio` | Design Studio emails and components | `design-studio` |
| `customerio-pipelines` | Sources, destinations, reverse ETL, data in/out | `cdp-api` |
| `customerio-sdk` | JS / mobile SDK install, sandbox, go-live | `cio` |

## Commands

| Command | Does |
| --- | --- |
| `/customerio:campaign-report` | Metrics + recommendations for an automation |
| `/customerio:build-segment` | Segment from a plain-English audience description |
| `/customerio:draft-email` | Design Studio draft with QA review |
| `/customerio:workspace-health` | Read-only deliverability/pipeline diagnosis |

## Docs

- Setup: https://docs.customer.io/ai/mcp/claude/
- Publishing this repo: [docs/PUBLISH.md](docs/PUBLISH.md)

## License

MIT — see [LICENSE](LICENSE).

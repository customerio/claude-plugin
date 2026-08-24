# Customer.io plugins for Claude

Official Customer.io plugin marketplace for **Claude Code** and **Cowork** —
the hosted MCP connector plus skills and slash commands for Journeys, Data
Pipelines, Design Studio, and SDK setup.

This repo mirrors the structure and philosophy of
[customerio/cursor-plugin](https://github.com/customerio/cursor-plugin):
skills in git are thin routers; the real playbooks live on the MCP server
(`cio_skills_read`) so they update with the product without a plugin release.

## Install

From the Claude plugin directory (once published), or directly as a marketplace:

```
/plugin marketplace add customerio/claude-plugin
/plugin install customerio@customerio
```

## What's inside

| Component | Purpose |
| --- | --- |
| MCP connector | Hosted server at `mcp.customer.io` (OAuth; home region selected after login) |
| `customerio` skill | Bootstrap: connect, prime, routing, safety rules |
| `customerio-journeys` | Automations, profiles, segments, broadcasts, transactional, in-app |
| `customerio-design-studio` | Design Studio emails, components, global styles |
| `customerio-pipelines` | CDP sources, destinations, reverse ETL |
| `customerio-sdk` | JS / mobile SDK install, sandbox, go-live |
| `/customerio:campaign-report` | Performance report for an automation |
| `/customerio:build-segment` | Segment from a plain-English audience |
| `/customerio:draft-email` | Design Studio email draft + QA review |
| `/customerio:workspace-health` | Read-only workspace diagnosis |

## Docs

- Setup: https://docs.customer.io/ai/mcp/claude/
- Publishing this repo: [docs/PUBLISH.md](docs/PUBLISH.md)

## License

MIT — see [LICENSE](LICENSE).

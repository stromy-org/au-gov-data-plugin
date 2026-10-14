# AU Gov Data

Australian government research inside your own AI tools: Hansard across every parliament, federal legislation, procurement, political finance and statistics, served by the AU Gov Data connector

## Prerequisites

- Claude Code v2.1.49+
- Node.js 18+, Python 3.11+ with [uv](https://docs.astral.sh/uv/)
- GitHub access to this repo (`gh auth login`)

## Installation

Via marketplace:
```bash
/plugin marketplace add stromy-org/au-gov-data-marketplace
/plugin install au-gov-data --marketplace stromy-org/au-gov-data-marketplace
```

For local development:
```bash
git clone https://github.com/stromy-org/au-gov-data-plugin.git
cd au-gov-data-plugin
npm install
uv sync
claude --plugin-dir .
```

## Connector

The Australian data itself comes from the **AU Gov Data** connector, an authenticated MCP server
(invitation-only, Microsoft sign-in). It is never declared in this plugin: add it once under
**Settings → Connectors** as a custom connector with the URL
`https://au-gov-data.braveforest-e73e8541.northeurope.azurecontainerapps.io/mcp`, then switch it on
in the chat. The `au-setup` skill walks through it step by step.

## Skills

Skills are split between MCP-hosted stubs (fetched at runtime from the AU Gov Data
connector) and the locally-authored `au-setup` skill. This plugin carries no client brand
overlay: it is a product plugin, not a client plugin.
See `skills/README.md` for the maintenance workflow.

## Maintenance

This plugin is a **product**, not a coding workspace: it ships no
agent-instruction files (no `AGENTS.md`/`CLAUDE.md`/copilot) and keeps only
`.mcp.json` (+ its `.agents/mcp.json` source) for MCP wiring. Maintaining it is
an operator task driven by the `plugin-maintain` skill in stromy-org
(`/plugin-maintain`, run against this plugin) — the skill is deliberately not
shipped here.

## Updating

```bash
/plugin update au-gov-data
```

## License

See [LICENSE](LICENSE) for terms.

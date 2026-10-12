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
/plugin install au-gov-data
```

For local development:
```bash
git clone https://github.com/stromy-org/au-gov-data-plugin.git
cd au-gov-data-plugin
npm install
uv sync
claude --plugin-dir .
```

## Skills

Skills are split between MCP-hosted stubs (fetched at runtime via
`ReadMcpResourceTool`) and locally-authored skills (frontmatter `_local: true`).
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

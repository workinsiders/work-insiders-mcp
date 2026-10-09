# Work Insiders MCP Server

Ask your AI assistant about 1,000+ recruiting, HR, sales prospecting and AI tools, with answers straight from the [Work Insiders](https://workinsiders.com) directory: starting prices with the date checked, side-by-side comparisons, alternatives and ATS integrations.

- **Server URL:** `https://workinsiders.com/mcp`
- **Transport:** Streamable HTTP, no authentication, free
- **Docs:** https://workinsiders.com/mcp-server/
- **Capabilities:** read-only. Every tool only reads public directory data. Nothing can be changed, sent or bought. No account, no keys, no sign-in.

## Tools

| Tool | What it does |
| ---- | ------------ |
| `workinsiders_search_tools` | Search the directory by free text and filters (category, first-party MCP server, API, free plan, free trial, AI-native, max starting price). Up to 25 tools per page. |
| `workinsiders_get_tool` | Full profile of one named tool: pricing with plans and date checked, free trial, MCP/API, AI features, strengths, watch-outs, pros/cons, integrations, Capterra rating, named alternatives. |
| `workinsiders_compare_tools` | Side-by-side comparison of 2 to 4 named tools. |
| `workinsiders_find_alternatives` | Alternatives to one named tool, filterable by MCP, free plan and price. |
| `workinsiders_list_categories` | Every Work Insiders category with slug, tool count and page link. |
| `workinsiders_category_overview` | What a category costs: tool count, median public starting price, editor picks, cheapest public prices. |
| `workinsiders_ats_integrations` | Which tools integrate with an ATS (Bullhorn, Greenhouse, Lever, Workday, JobAdder and others), with vendor confirmation and sync direction. |

## Connect

**Claude (web/desktop):** Settings → Customize → Connectors → Add custom connector, name it "Work Insiders", paste the server URL. No sign-in needed.

**Claude Code:** `claude mcp add --transport http work-insiders https://workinsiders.com/mcp`, then `/mcp` to verify.

**Grok:** grok.com/connectors → New Connector → Custom → paste the server URL.

**Cursor:** Settings → MCP → add to `mcp.json`: `{"mcpServers":{"work-insiders":{"url":"https://workinsiders.com/mcp"}}}`.

**ChatGPT / VS Code / others:** add a custom connector or remote (HTTP) MCP server with the URL above.

## Registry files

- `server.json` - listing metadata for the [Official MCP Registry](https://registry.modelcontextprotocol.io)
- `lhm.plugin.json` - listing metadata for the [LobeHub Marketplace](https://lobehub.com/mcp)
- `.github/workflows/publish-registry.yml` - publishes to the official registry on push

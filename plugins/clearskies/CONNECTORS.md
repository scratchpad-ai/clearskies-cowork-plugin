# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for the tool the user connects in that category. For example, `~~CRM` refers to Salesforce as configured inside the Clearskies Context Graph.

Unlike most plugins, this one routes through a single MCP server — Clearskies — which aggregates your connected tools into one unified layer. The integrations below are configured inside your Clearskies account, not in `.mcp.json`.

## Connectors for this plugin

| Category | Placeholder | Supported via Clearskies |
|----------|-------------|--------------------------|
| Context Graph | `~~context graph` | Clearskies |
| CRM | `~~CRM` | Salesforce |
| Conversation intelligence | `~~conversation intelligence` | Gong, Scratchpad |
| Email | `~~email` | Gmail, Microsoft 365 |
| Calendar | `~~calendar` | Google Calendar, Microsoft 365 |
| Chat | `~~chat` | Slack |

## How Clearskies handles integrations

Unlike most plugins that connect directly to each tool via separate MCP servers, this plugin routes through the **Clearskies Context Graph** — a unified layer that aggregates CRM records, call transcripts, emails, calendar events, and Slack threads into a single queryable surface.

This means:
- The only required MCP server is `clearskies`
- Integrations like Salesforce, Gong, and Slack are configured inside your Clearskies account, not in `.mcp.json`
- Skills and commands query the Context Graph rather than individual tools directly

To connect your integrations, visit [clearskies.cc](https://clearskies.cc) and configure your sources in the integrations settings.

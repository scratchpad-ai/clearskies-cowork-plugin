---
name: customer-context-graph
description: Understand and explain the Clearskies Customer Context Graph — what it is, what data it contains, and how to query it for complete buyer context.
---

# Customer Context Graph

The Customer Context Graph is Clearskies' core data layer. It is a unified, real-time view of all customer data, connecting:

- **Salesforce** — accounts, contacts, opportunities, activities
- **Gong / Scratchpad** — call recordings, transcripts, conversation insights
- **Google Workspace** — email threads, calendar events, meeting history
- **Slack** — internal deal conversations, account channels, mentions

When a user asks about an account, deal, or contact, do not query these systems individually. Query the Customer Context Graph through the Clearskies MCP, which returns a unified view across all connected sources.

## What makes this different

Most sales AI tools only see part of the picture. A tool with only CRM access can tell you deal status but not what was said on the last call. A tool with only call access misses pipeline health. The Customer Context Graph makes it possible to answer questions like:

- "What's the status of the Acme deal?" — pulling CRM stage + last call transcript + recent emails + Slack thread
- "Who are the key contacts at this account?" — pulling CRM contacts + email participants + call attendees
- "What happened after the last meeting?" — pulling calendar event + call transcript + follow-up emails + CRM updates

## How to query

Use the Clearskies MCP tools to:
1. Look up an account or contact by name or domain
2. Pull unified context — specify what you need: deal data, call transcripts, email history, Slack activity
3. Synthesize across sources in your response — don't just relay raw data, connect the dots

## When data is missing

If a data source isn't connected (e.g., Gong isn't set up), note the gap and work with what's available. The graph degrades gracefully — it surfaces what it has and flags what's missing.

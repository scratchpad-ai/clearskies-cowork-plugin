# Clearskies Sales Plugin

A sales intelligence plugin for [Cowork](https://claude.com/product/cowork) and Claude Code. Built for the Clearskies team — gives you full account context, deal risk scoring, post-call workflows, and personalized outreach without leaving your workflow.

Works standalone with web search and your input. Supercharged when you connect your CRM, email, calendar, and call transcripts.

---

## Installation

```bash
claude plugins add clearskies
```

---

## Commands

Explicit workflows you invoke with a slash command:

| Command | Description |
|---|---|
| `/account-brief` | Full account brief — company overview, stakeholders, deal history, recommended approach |
| `/call-prep` | Prepare for an upcoming call — agenda, discovery questions, account context, attendee research |
| `/deal-risk` | Score deal health — flag risks, identify gaps, surface a recommended action plan |
| `/pipeline-review` | Review pipeline health — prioritize deals, flag stale and stuck opportunities, get a weekly action plan |
| `/post-call` | Process call notes or transcript — action items, internal summary, draft follow-up email |
| `/draft-outreach` | Research a prospect and draft personalized outreach — email and LinkedIn |

---

## Skills

Domain knowledge Claude uses automatically when relevant:

| Skill | Description |
|---|---|
| `customer-context-graph` | Builds a holistic view of an account — org chart, relationships, sentiment, history, open items |
| `account-research` | Web + enrichment research on a company or contact — news, signals, key people, recommended angle |
| `deal-risk` | Evaluates deal health and scores risk factors — MEDDIC gaps, stakeholder coverage, activity signals |
| `call-prep` | Synthesizes account context into a pre-call brief — agenda, questions, prior history |
| `post-call-workflow` | Structures raw notes or transcripts into summaries, action items, and follow-up drafts |
| `draft-outreach` | Research-first outreach — researches prospect before drafting, generates personalized email + LinkedIn |

---

## Example Workflows

### Before a Call

```
/call-prep Acme Corp — discovery call tomorrow with their VP Eng and CTO
```

Get a full pre-call brief: company overview, attendee research, prior history, suggested agenda, discovery questions, and objection prep.

### After a Call

```
/post-call
[paste notes or transcript]
```

Get a structured internal summary, action items with owners and due dates, and a draft follow-up email ready to send.

### Scoring a Deal

```
/deal-risk Acme Corp
```

Get a risk score across MEDDIC dimensions, activity signals, stakeholder coverage, and a prioritized list of gaps to close.

### Reviewing Pipeline

```
/pipeline-review
```

Upload a CSV or describe your pipeline. Get a health score, deal prioritization, risk flags, and a weekly action plan.

### Researching a Prospect

Just ask naturally:

```
Research Acme Corp before my call tomorrow
```

The `account-research` skill triggers automatically and delivers company overview, key contacts, recent news, and a recommended approach.

### Drafting Outreach

```
Draft an email to the VP of Engineering at TechStart
```

The `draft-outreach` skill researches the prospect first, then generates personalized outreach with multiple subject line options.

---

## Standalone + Supercharged

Every command and skill works without any integrations:

| What You Can Do | Standalone | Supercharged With |
|---|---|---|
| Account research | Web search | Enrichment MCP (Clay, Apollo, ZoomInfo) |
| Call prep | Describe meeting, paste context | CRM, Email, Calendar, Transcripts MCPs |
| Deal risk scoring | Describe deal | CRM (deal data, activity) |
| Pipeline review | Upload CSV, paste deals | CRM MCP |
| Post-call processing | Paste notes / transcript | Transcripts MCP, CRM, Email |
| Draft outreach | Web search + your context | Enrichment, CRM, Email MCPs |
| Account context graph | Manual input | CRM, Email, Transcripts, Slack |

---

## MCP Integrations

Configure connectors in `.mcp.json`. Supported integrations:

| Category | Examples | What It Enables |
|---|---|---|
| **CRM** | HubSpot, Salesforce, Close | Deal data, contact records, account history |
| **Email** | Gmail, Outlook | Thread history, follow-up drafting, send |
| **Calendar** | Google Calendar, Outlook | Meeting context, attendee lookup |
| **Transcripts** | Gong, Fireflies, Chorus | Call recordings, transcript extraction |
| **Enrichment** | Apollo, Clay, ZoomInfo | Verified contact data, company intel |
| **Chat** | Slack, Teams | Internal account discussions, colleague intel |

---

## Team Configuration

Edit `clearskies.local.md` to add team-specific context that personalizes all commands and skills:

- Your name, title, and quota
- Product positioning and value props
- Competitor talk tracks
- ICP definition
- Proof points and customer stories

This file is gitignored by default — it stays local to your machine.

---

## Settings

Create `.claude/settings.local.json` to configure personal preferences:

```json
{
  "name": "Your Name",
  "title": "Account Executive",
  "quota": {
    "annual": 1000000,
    "quarterly": 250000
  },
  "territory": "Mid-Market, West",
  "product": {
    "name": "Clearskies",
    "value_props": [
      "Key value proposition 1",
      "Key value proposition 2"
    ],
    "competitors": [
      "Competitor A",
      "Competitor B"
    ]
  }
}
```

The plugin will ask you for this information interactively if it's not configured.

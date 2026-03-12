# Clearskies Plugin

An agent builder for revenue teams, available as a plugin for [Cowork](https://claude.com/product/cowork) and Claude Code. Connects your Context Graph to Claude — giving your GTM team full account context, deal risk scoring, post-call workflows, and personalized outreach without leaving their workflow. Works standalone with web search and your input. Supercharged when you connect your CRM, email, calendar, and call transcripts.

---

## Installation

```bash
claude plugin install clearskies@scratchpad-ai/clearskies-cowork-plugin
```

---

## Commands

Explicit workflows you invoke with a slash command:

| Command | Description |
|---|---|
| `/account-brief` | Full account brief — company overview, stakeholders, deal history, recommended approach |
| `/call-prep` | Complete pre-call brief — account snapshot, open items, contact context, suggested agenda, key opening question |
| `/deal-review` | Paranoid deal audit — champion engagement, economic buyer status, unanswered comms, close date health, velocity |
| `/deal-strategy` | CRO-mode strategy — find the one move that changes the deal, what must be true to close, when to push or qualify out |
| `/meddic` | Evidence-based MEDDIC audit — score every criterion against real signals, not rep self-reporting |
| `/pipeline-review` | Pipeline health ranked by urgency — engagement drops, stalled close dates, missing stakeholders, action plan |
| `/post-call` | Process call notes or transcript — action items, internal summary, draft follow-up email |
| `/rep-coaching` | Pull transcripts, surface coaching moments with timestamps, identify patterns, draft 1:1 feedback |
| `/draft-outreach` | Research a prospect and draft personalized outreach — email and LinkedIn |

---

## Skills

Domain knowledge Claude uses automatically when relevant:

| Skill | Description |
|---|---|
| `customer-context-graph` | Builds a holistic view of an account — org chart, relationships, sentiment, history, open items |
| `account-research` | Web + enrichment research on a company or contact — news, signals, key people, recommended angle |
| `call-prep` | Synthesizes account context into a complete pre-call brief — snapshot, open items, agenda, key opening question |
| `deal-review` | Paranoid deal audit — surfaces risk signals across champion, economic buyer, comms, close date, velocity |
| `deal-strategy` | CRO-mode deal reasoning — situation assessment, the move, what must be true, push/qualify out recommendation |
| `meddic` | Evidence-based MEDDIC qualification — scores each criterion against actual call and email data, not CRM fields |
| `post-call-workflow` | Structures raw notes or transcripts into summaries, action items, and follow-up drafts |
| `rep-coaching` | Surfaces behavioral patterns across calls with timestamped quotes, and drafts specific written coaching feedback |
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

### Auditing a Deal

```
/deal-review Acme Corp
```

Get a signal-by-signal audit of everything that can still kill the deal — champion engagement trend, economic buyer status, unanswered emails, close date decay — with an overall health rating and one recommended action.

### Running a MEDDIC Audit

```
/meddic Acme Corp
```

Get each MEDDIC criterion scored GREEN / YELLOW / RED against real evidence from calls, emails, and CRM — not rep self-reporting. Ends with a forecast recommendation and the specific gaps to close before it belongs in the commit.

### Getting Deal Strategy

```
/deal-strategy Acme Corp
```

Get a one-paragraph situation assessment (no hedging), the one move that changes the deal, three things that must be true to close with owners and dates, and an explicit recommendation to push the date or qualify out if any are unlikely.

### Coaching a Rep

```
/rep-coaching Alex — last 3 Acme calls
```

Get recurring behavioral patterns across calls, 2–3 specific coaching moments with timestamps and exact quotes, what to say to the rep, and a draft 1:1 feedback note ready to send.

### Reviewing Pipeline

```
/pipeline-review
```

Get a pipeline ranked by urgency — not close date. Engagement drops, frozen close dates, missing economic buyers, and a weekly action plan sorted by what actually needs attention.

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
| Account research | Web search | Salesforce, Gong, Scratchpad |
| Call prep | Describe meeting, paste context | Salesforce, Google, Microsoft, Gong, Scratchpad |
| Deal review | Describe deal + recent activity | Salesforce, Gong, Scratchpad, Slack |
| Deal strategy | Describe deal + gaps | Salesforce, Gong, Scratchpad |
| MEDDIC audit | Describe deal + qualification | Salesforce, Gong, Scratchpad |
| Pipeline review | Upload CSV, paste deals | Salesforce |
| Rep coaching | Paste transcripts | Gong, Scratchpad |
| Post-call processing | Paste notes / transcript | Gong, Scratchpad, Salesforce, Google, Microsoft |
| Draft outreach | Web search + your context | Salesforce, Google, Microsoft |
| Context graph | Manual input | Salesforce, Gong, Scratchpad, Google, Microsoft, Slack |

---

## MCP Integrations

Configure connectors in `.mcp.json`. Supported integrations:

| Integration | What It Enables |
|---|---|
| **Salesforce** | Deal data, contact records, account history |
| **Gong** | Call recordings, transcript extraction |
| **Scratchpad** | Call recordings, transcript extraction |
| **Google** | Email threads, calendar, meeting context |
| **Microsoft** | Email threads, calendar, meeting context |
| **Slack** | Internal account discussions, colleague intel |

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

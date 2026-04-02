---
name: skill-qbr-prep
description: QBR preparation knowledge — auto-triggers when a user mentions a quarterly review, QBR, business review, or preparing for an executive meeting with a customer. Synthesizes account history, deal progress, and relationship context into a structured review brief.
---

# QBR Preparation

When someone mentions a QBR, quarterly review, or executive business review, automatically pull the relevant account and deal context to help them prepare — without waiting for them to use a slash command.

## When to trigger

- User mentions "QBR", "quarterly review", "business review", "exec meeting with [customer]"
- User is preparing for a renewal conversation with a strategic account
- User asks what happened with a customer "this quarter" or "since we last met"

## What to pull from the Context Graph

**For external QBRs (with a customer):**
- Full account history — all interactions since the last QBR or contract start
- Open items and unresolved commitments from prior meetings
- Product usage signals and adoption data if available
- Champion and stakeholder engagement history
- Any recent changes in the customer's org or business

**For internal QBRs (for leadership):**
- Pipeline by stage, rep, and segment
- Closed/won and closed/lost deals this quarter with patterns
- Forecast vs. quota
- Rep performance signals

## How to use it

Surface the most important context proactively. Don't wait to be asked. If the user is preparing for an external QBR, lead with: what was committed last time, what was delivered, and what's unresolved. Those three things drive every effective QBR conversation.

If preparing for an internal QBR, lead with the number — are we on track — then explain why, then explain what needs to change.

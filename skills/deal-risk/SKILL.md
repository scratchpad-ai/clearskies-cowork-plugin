---
name: deal-risk
description: Monitor and assess deal risk using Customer Context Graph signals — engagement drops, champion changes, stalled stages, and other warning signs.
---

# Deal Risk Assessment

When asked to assess pipeline risk or identify at-risk deals, use the Customer Context Graph to look for signals across all data sources — not just CRM stage.

## Risk signals to look for

**Engagement signals (from calls, email, calendar, Slack)**
- No contact in 30+ days with an open deal
- Drop in email response rate or response time
- Meetings scheduled and then cancelled
- Calls getting shorter or less frequent
- Key contacts going silent

**Relationship signals (from CRM + calls)**
- Champion has left or changed roles
- New stakeholder appearing late in the deal
- Executive sponsor disengaged

**Deal hygiene signals (from CRM)**
- Close date slipped multiple times
- Stage hasn't moved in 30+ days
- No next step or next meeting logged
- Missing key qualification fields (MEDDPICC gaps, BANT gaps, etc.)

**Conversation signals (from Gong / Scratchpad transcripts)**
- Competitor mentioned repeatedly
- Pricing concerns raised but not resolved
- "Let me check with my team" with no follow-up
- Decision timeline shifted

## Output format

For each at-risk deal:
- **Deal**: name, stage, value, close date
- **Risk level**: High / Medium / Low
- **Top signal**: the single most important warning sign
- **Supporting signals**: 2-3 additional data points
- **Recommended action**: specific next step

Sort by risk level, then by deal value.

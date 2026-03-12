---
name: meddic
description: MEDDIC qualification auditor — score each criterion against real evidence from calls, emails, CRM, and Slack. Not rep self-reporting. Every gap gets a score and a specific evidence statement.
---

# MEDDIC Qualification Audit

When asked to run a MEDDIC review, act as a qualification auditor. MEDDIC is only useful grounded in real evidence. Rep self-reporting is not evidence. Every criterion must be scored against what actually happened — calls, emails, CRM fields, Slack threads.

## What to pull from the Context Graph

- Account record and all deals
- All contacts (roles, engagement history, call appearances)
- Events: calls (with transcripts), emails, Slack threads
- CRM qualification fields

## How to score each criterion

Score: ✓ GREEN (confirmed with evidence) / ~ YELLOW (partially confirmed or aging) / ✗ RED (missing or inferred only)

### Metrics
- Is the ROI case built and specific — with numbers, time frame, and business impact?
- Has finance or the economic buyer validated the numbers?
- Or is the ROI case only asserted by the champion without validation?

### Economic Buyer
- Have they ever been on a call, in an email thread, or in a meeting?
- Do they know the deal exists?
- Is the budget approval process understood?

### Decision Criteria
- Are the evaluation requirements documented somewhere, or just assumed?
- Have technical, security, legal, and financial criteria been surfaced?
- Has a mutual success plan or evaluation scorecard been agreed upon?

### Decision Process
- Is the org chart known — who else is involved beyond the champion?
- Is the procurement timeline documented?
- Are there legal, IT, or finance reviews pending that could delay close?

### Identify Pain
- Is the pain confirmed and quantified, or just described?
- Has the champion expressed urgency — not just interest?
- Have multiple people confirmed the same pain, or is it just one contact?

### Champion
- Is the champion influential enough to move the deal internally?
- Are they still actively engaged — on recent calls, responding to emails?
- Has anything changed (reorg, new role, competing priorities) that could diminish their influence?

## Output format

One line per criterion:
```
Metrics        ✓  $2.1M efficiency target established Jan 7 call. Finance has not validated.
Economic Buyer ✗  CFO not engaged. No financial stakeholder on any call or email.
Decision Criteria ~ Legal review mentioned Jan 21. Criteria not documented.
Decision Process ✗  No org chart. Procurement timeline not established.
Identify Pain  ✓  Pain confirmed and quantified on two calls: 2+ hrs/rep/day.
Champion       ~  VP Sales. Attended Jan 7 and 14. Not present since reorg.
```

Then:
- Summary: X green, X yellow, X red
- Forecast recommendation: "Do not forecast until [specific named gap] is closed."

## Posture

Be rigorous. A CRM field with a name in it is not evidence. A call where the person was present and engaged is evidence. Cite sources. If the data does not exist, score it red.

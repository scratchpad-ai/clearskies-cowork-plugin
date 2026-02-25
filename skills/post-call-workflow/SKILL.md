---
name: post-call-workflow
description: After a call, extract action items, draft follow-up communications, generate a CRM summary, and identify what needs to be updated — all from the call transcript in the Customer Context Graph.
---

# Post-Call Workflow

When asked to process a call or handle post-call work, pull the call transcript from the Customer Context Graph (Gong or Scratchpad) and execute the full workflow.

## Steps

1. **Pull the transcript** from the Customer Context Graph — find the most recent call for the account, or the specific call if identified
2. **Extract action items** — what was promised, by whom, by when
3. **Identify next steps** — what was agreed for moving forward
4. **Flag CRM updates needed** — stage change? New contact? Close date updated?
5. **Draft follow-up email** — grounded in what was actually discussed, not generic

## Output format

**Call Summary**
- Date, attendees, duration
- 3-5 sentence summary of what was discussed

**Action Items**
- [ ] [Owner]: [action] by [date]

**CRM Updates Needed**
- [Field]: [current value] → [suggested update] — [reason]

**Draft Follow-Up Email**

Subject: [specific to what was discussed]

[Personalized email that references specific topics from the call, confirms next steps, and makes it easy for the prospect to respond]

Keep the email under 150 words. Reference something specific from the call in the first sentence.

# Discovery Call Preparation Workflow

**Purpose:** Generate a structured discovery call plan — including your call objective, the question arc, hypothesis to test, and the specific things to listen for — before a first or second discovery conversation.

**Context files required:** `01-company-context.md`, `02-icp-definition.md`, `03-persona-cards.md`, `04-competitive-positioning.md`

**Time to run:** 10–15 minutes (AI execution) + 10 minutes (rep review)

**When to use:** After the pre-sale intelligence brief (run that first if you haven't). This workflow turns research into a call structure.

**Note:** Run the pre-sale intelligence workflow first (`02-presale-intelligence/account-research-workflow.md`) and have that output available. The discovery prep is more useful when it builds on account-specific intelligence.

---

## What You Need Before Running

- Account name and primary contact (name, title, time in role)
- Meeting type: [First discovery / Second discovery / Multi-stakeholder call]
- Who will be in the room: [List everyone joining from the prospect side]
- Your call objective: [What specific outcome do you need from this call to advance the deal? Be precise — not "learn about them" but "confirm budget authority and identify the economic buyer"]
- Pre-sale intelligence output (if available): [Paste the key hypotheses and trigger events from Step 1 and 2 of the pre-sale workflow]

---

## The Prompt

**Copy and paste into your Claude Project. Fill in all bracketed fields.**

---

```
Using the context files loaded in this project, generate a discovery call preparation plan for the following meeting.

Account: [Company name]
Primary contact: [Name], [Title], [X months in role]
Others on the call from their side: [List names and titles, or "Unknown"]
Meeting type: [First discovery / Second discovery / Multi-stakeholder]
My call objective: [What I need to confirm or advance by end of this call]

Pre-sale context summary (paste from pre-sale brief if available, or summarize what you know):
[Paste or summarize]

Generate the following:

1. CALL OBJECTIVE (sharpened)
Restate my call objective more precisely, given what we know about this account. If my stated objective is too vague or misaligned with what's achievable in a first call, flag it and suggest a tighter version.

2. HYPOTHESIS TO TEST
The single most important unknown I need to resolve in this call. State it as a hypothesis: "I believe [X] is true for this account. I will know I'm right if they say [Y]."

3. QUESTION ARC (5–7 questions in sequence)
A logical progression through the conversation, from opening to close:
- Opening question: Opens the conversation and invites them to share their situation
- Situation questions (2–3): Understand current state, existing processes, and what's working
- Problem questions (1–2): Surface the pain and its consequences
- Implication question (1): Help them articulate what happens if nothing changes
- Qualification question (1): Confirm budget authority, timeline, or decision process (choose the most critical unknown)

For each question: state the question, what you're listening for, and a follow-up if they give a surface-level answer.

4. MULTI-STAKEHOLDER NAVIGATION (if multiple people on their side)
For each person attending from their side:
- Their likely agenda for this call
- What they need to hear to feel good about the conversation
- What could make them disengage or become skeptical

5. CALL CLOSE
What you will say in the last 5 minutes to:
- Summarize what you heard (in their language)
- Confirm the next step (specific date, not "I'll follow up")
- Set up the next conversation with the right framing

6. RED FLAGS TO WATCH FOR
Two or three signals during the call that would change your assessment of this opportunity — either raising or lowering your confidence.
```

---

## After the Call: Quick Debrief Prompt

Run this immediately after the call, while it's fresh. Paste your raw notes and let Claude structure the debrief.

---

```
I just completed a discovery call with [Name] at [Company]. Here are my raw notes:

[Paste your notes]

Using our context files, generate:

1. HYPOTHESIS UPDATE
Did the call confirm or disconfirm the hypothesis we set out to test? What did they actually say?

2. PAIN CONFIRMED OR REVISED
Based on what they said, which of our original pain hypotheses holds? What did we learn that we didn't expect?

3. QUALIFICATION ASSESSMENT
Based on this call, rate this opportunity: Strong fit / Qualified with questions / Not yet qualified / Disqualified
Explain in 2–3 sentences.

4. NEXT STEP BRIEF
What is the specific next step, who owns it, and what needs to happen before the next call?

5. CRM UPDATE (2–3 sentences)
A clean, professional summary to paste into Salesforce / HubSpot notes.
```

---

**Quality gate before the call:**
- [ ] Call objective is specific and achievable in this meeting
- [ ] Questions are open-ended and don't telegraph our solution
- [ ] You've reviewed the multi-stakeholder section if more than one person is attending
- [ ] You know your call close — how you'll land the next step before the call ends

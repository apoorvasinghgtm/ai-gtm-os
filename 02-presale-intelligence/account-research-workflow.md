# Pre-Sale Account Intelligence Workflow

**Purpose:** Generate a structured pre-sale intelligence brief for a specific account before a discovery or follow-up call. Compresses 3–4 hours of manual research into a 15-minute rep review.

**Context files required:** `01-company-context.md`, `02-icp-definition.md`, `03-persona-cards.md`, `04-competitive-positioning.md`, `05-proof-library.md`

**Time to run:** 15–20 minutes (AI execution) + 15 minutes (rep review)

**When to use:** Before any first discovery call, re-engagement call, or significant follow-up where deal context has changed.

---

## Overview

This is a three-step prompt chain. Run each step in sequence in your Claude Project. Each step builds on the previous one — do not skip steps or run them out of order.

| Step | What It Produces | Human Review Before Next Step |
|------|-----------------|-------------------------------|
| Step 1 | Account situation analysis | Verify trigger events are current |
| Step 2 | Pain point hypotheses + discovery questions | Confirm hypotheses match what you know |
| Step 3 | Competitive context + ROI anchor + call opener | Confirm proof point is approved for use |

---

## Before You Run: What You Need

Gather the following before running Step 1. The more complete this is, the more useful the output.

- **Account name:** [Company name]
- **Primary contact:** [Name, title, how long they've been in role]
- **Meeting type:** [First discovery / Re-engagement / Follow-up / Eval stage]
- **What you know so far:** [Any notes from previous calls, emails, or CRM history — paste here]
- **How they found us / inbound signal:** [e.g., Downloaded a piece of content, inbound form, referral, cold outreach response]
- **Deal stage:** [Where this sits in your pipeline, if applicable]

Optional but valuable:
- Any intent data signals you have on this account
- Recent news about the company you've noticed

---

## Step 1: Account Situation Analysis

**Copy and paste this prompt into your Claude Project. Fill in the bracketed fields.**

---

```
Using the context files loaded in this project, generate an account situation analysis for the following prospect.

Account: [Company name]
Primary contact: [Name], [Title] — [X months/years] in this role
Meeting type: [First discovery / Re-engagement / Follow-up]
What I know so far: [Paste your notes, or write "No prior contact"]
Inbound signal: [How they engaged, or write "Outbound — no inbound signal"]

Produce the following:

1. COMPANY SNAPSHOT (3–5 bullets)
Key facts about this company's current state — size, stage, recent growth or contraction signals, business model, and market position. Be specific; avoid generic descriptions.

2. TRIGGER EVENTS (list all you can identify, with rough timing)
Recent changes that create urgency or relevance for our product: leadership changes, funding events, headcount growth or reduction, public statements about the problem we solve, technology changes, competitive moves.

3. STAKEHOLDER CONTEXT (for the primary contact listed above)
Based on their title and time in role, what are the most likely goals, pressures, and success metrics for this person right now? Cross-reference with our persona cards. What's their likely mandate in this role?

4. TIMING RISKS AND INTERNAL FRICTION (2–3 bullets)
What factors might slow this deal down or make the timing bad? Examples: recent layoffs, exec transition, Q4 budget freeze, competitor already entrenched.

Keep this section to one page. Flag any area where you're making an inference rather than drawing from stated facts.
```

---

**Before moving to Step 2, review:**
- [ ] Trigger events reflect current reality (not outdated news)
- [ ] Stakeholder context is consistent with what you know about this contact
- [ ] No factual claims you can't verify or ask about in the call

---

## Step 2: Pain Point Hypotheses and Discovery Prep

**Copy and paste this prompt. Run it in the same conversation as Step 1 — Claude has the account context from Step 1.**

---

```
Based on the account situation analysis above and the persona cards and ICP definition in your context files, generate the following:

1. THREE PAIN POINT HYPOTHESES (ranked by likelihood)
For each hypothesis:
- State the pain in buyer language (how they would describe it, not how we describe our solution)
- Explain the evidence from Step 1 that supports this hypothesis
- Note what would confirm or disconfirm it in the call

2. FIVE DISCOVERY QUESTIONS
Questions designed to confirm or disprove the hypotheses above. Each question should:
- Be open-ended (not yes/no)
- Invite the prospect to tell you something you don't already know
- Not telegraph our product's solution
- Be sequenced — questions 1–2 open the conversation, 3–4 go deeper, question 5 is for executive alignment or budget reality

3. LISTENING PRIORITIES
Three things to specifically listen for during the call that would meaningfully change your assessment of this opportunity.

4. FALSE ASSUMPTIONS TO AVOID
One or two assumptions that would be easy to make about this account or contact based on the data — but that could be wrong and would undermine the call if you acted on them unchecked.
```

---

**Before moving to Step 3, review:**
- [ ] Pain hypotheses reflect what you already know about this contact — nothing that would obviously miss
- [ ] Discovery questions feel natural, not scripted
- [ ] No question reveals proprietary information about our sales process

---

## Step 3: Competitive Context and ROI Anchor

**Copy and paste this prompt. Run it in the same conversation.**

---

```
Based on the account situation and pain hypotheses above, generate the following:

1. COMPETITIVE CONTEXT
What alternatives is this prospect most likely evaluating or currently using?
- Most likely competitor or status quo (based on their profile)
- How to position against it using our approved competitive positioning
- One thing NOT to say that could backfire with this specific account

2. ROI ANCHOR
Select the single most resonant proof point from our proof library for this prospect and contact.
- State the proof point
- Explain why it's the right one for this specific persona and situation
- Suggest the moment in the conversation to introduce it (never lead with it)

3. SUGGESTED CALL OPENER (2–3 sentences)
A credibility-establishing opening that:
- Acknowledges something specific about their situation (from Step 1)
- Does not pitch the product
- Opens a diagnostic conversation
- Matches our voice and tone guidelines

Do not use the opener if the trigger event or situation detail hasn't been verified first.
```

---

**Before using this brief in a real call, complete this quality gate:**

- [ ] All trigger events in the brief are current (within last 60–90 days where timing matters)
- [ ] Pain hypotheses are grounded in what you know, not pure inference
- [ ] Competitive claims match approved positioning in `04-competitive-positioning.md`
- [ ] Proof point is approved for external use in `05-proof-library.md`
- [ ] Call opener doesn't sound scripted when you say it out loud
- [ ] You could defend every factual claim in this brief if asked

---

## Worked Examples

See `worked-examples/meridian-gtm/presale-brief-example.md` for a complete output example using the Meridian GTM fictional company in the RevTech vertical.

See `worked-examples/talentflow-ai/presale-brief-example.md` for a complete output example in the HRTech vertical.

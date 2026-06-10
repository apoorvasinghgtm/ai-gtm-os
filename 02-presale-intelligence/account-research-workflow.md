# Pre-Sale Intelligence Workflow

**Status: Stable**

---

## The problem this solves

A prepared rep is not a rep who spent four hours on Google before a meeting. A prepared rep is a rep who walks in knowing the three things most likely to matter to this specific buyer, at this specific company, at this specific moment — and has thought through how to use that knowledge.

Before AI, getting to that level of preparation took a skilled rep 3–4 hours per account. Most reps didn't do it consistently. The ones who did were manually triangulating across LinkedIn, news searches, the CRM, call recordings, and their own memory.

This workflow compresses that to 15 minutes of human review on top of an AI-generated brief — without sacrificing the depth that makes preparation actually useful.

---

## What this workflow produces

A **Pre-Sale Intelligence Brief**: a structured document a rep reads in 10–15 minutes before a meeting that gives them:

- Account context and current situation
- Stakeholder map with role-specific priorities
- Relevant trigger events and what they signal
- Three most likely pain points to probe in discovery
- Competitive context if applicable
- Suggested discovery questions calibrated to the buyer
- ROI anchor — the proof point most likely to land with this persona

---

## Inputs required

| Input | Source | Required? |
|---|---|---|
| Company name | Rep / CRM | Required |
| Primary contact name and title | Rep / CRM | Required |
| Meeting type (first call, demo, EBR) | Rep | Required |
| Deal stage and history | CRM | Required |
| Recent call notes or Gong summary | Gong / CRM | Strongly recommended |
| Intent data signals | 6sense / Bombora | If available |
| Any known context from the rep | Rep | High value |

---

## Context to load before running

Load the following files from your context layer before running this prompt:

- `company.md` — your product, differentiators, what you are not
- `icp.md` — ICP definition and trigger signals
- `personas.md` — persona cards for the primary contact's role
- `competitive.md` — if a competitor has been mentioned in prior touches
- `proof.md` — proof points organized by persona and outcome

---

## The prompt chain

This workflow runs in three sequential steps. Do not collapse them into one prompt — the quality degrades significantly when you do. [certain, based on testing]

---

### Step 1 — Account Situation Analysis

**Purpose:** Establish what's actually happening at this company right now — not generic background, but signals relevant to a buying decision.

```
You are preparing a pre-sale intelligence brief for a B2B sales rep.

COMPANY CONTEXT:
[paste company.md]

ICP DEFINITION:
[paste icp.md]

ACCOUNT TO RESEARCH:
Company: [company name]
Primary contact: [name], [title]
Meeting type: [first call / discovery / demo / EBR]
Deal stage: [stage]
Known context from rep: [any notes]

Using publicly available information and the inputs above, produce an Account Situation Analysis covering:

1. COMPANY SNAPSHOT (3–4 sentences)
   Current business situation, recent news, growth trajectory, anything that signals urgency or timing.

2. TRIGGER EVENTS (list up to 5)
   Recent events that are relevant to a buying decision — leadership changes, funding, hiring patterns, 
   product launches, earnings commentary, competitive moves. For each: state the event, the date if known, 
   and what it signals about buying readiness or priority.

3. STAKEHOLDER CONTEXT
   Based on the contact's title and tenure, what are the most likely priorities, pressures, and success 
   metrics for this person right now? What does winning look like for them in the next 90 days?

4. RISK FLAGS
   Anything that suggests poor timing, internal friction, or a reason this deal might stall.

Format as structured sections. Be specific — no generic statements that could apply to any company.
```

---

### Step 2 — Pain Point Hypotheses and Discovery Prep

**Purpose:** Translate the account situation into a specific discovery strategy — what to probe, what to listen for, what not to assume.

```
You are preparing the discovery strategy section of a pre-sale intelligence brief.

ACCOUNT SITUATION ANALYSIS:
[paste output from Step 1]

PERSONA CONTEXT:
[paste relevant persona card from personas.md]

PRODUCT CONTEXT:
[paste company.md]

Based on the account situation and persona context, produce:

1. THREE PAIN POINT HYPOTHESES
   The three pain points most likely to be true for this buyer at this company right now, 
   ranked by probability. For each:
   - State the hypothesis in the buyer's language (not our product language)
   - Explain why the account signals support this hypothesis
   - Note what would confirm or disconfirm it in discovery

2. FIVE DISCOVERY QUESTIONS
   Questions designed to surface the true pain points — not leading questions that telegraph 
   our product, but genuine diagnostic questions that help the rep understand whether and 
   where we fit. Each question should:
   - Be open-ended
   - Map to one of the pain point hypotheses
   - Feel natural in a first conversation, not like a qualification checklist

3. LISTEN FOR
   Three things the rep should pay close attention to in this conversation — signals that 
   indicate urgency, budget authority, or competitive consideration.

4. AVOID ASSUMING
   Two assumptions that would be easy to make based on the account profile but could 
   be wrong — and why walking in with those assumptions would hurt the conversation.
```

---

### Step 3 — Competitive Context and ROI Anchor

**Purpose:** Equip the rep with the competitive framing and proof point most likely to matter in this specific conversation.

```
You are completing a pre-sale intelligence brief with competitive context and an ROI anchor.

ACCOUNT SITUATION:
[paste Step 1 output]

PERSONA CONTEXT:
[paste relevant persona card]

COMPETITIVE CONTEXT:
[paste competitive.md — or note "no competitor mentioned yet"]

PROOF LIBRARY:
[paste proof.md]

Produce:

1. COMPETITIVE POSTURE (if a competitor has been mentioned or is likely given the account profile)
   - Most likely competitor in this deal based on account signals
   - Where we win vs. them in this specific context
   - One thing NOT to say about the competitor (keeps us credible)

2. ROI ANCHOR
   The single proof point from our proof library most likely to resonate with this 
   persona at this company — and why. Include:
   - The proof point itself
   - The reason it lands with this buyer specifically
   - How to introduce it naturally (not as a data dump)

3. SUGGESTED OPENING
   A one-paragraph suggested opening for the call that acknowledges what we know about 
   their situation, establishes credibility without pitching, and opens a genuine 
   diagnostic conversation.
   Note: This is a starting point for the rep to personalize — not a script.
```

---

## Review gate

Before using the brief, the rep verifies:

- [ ] Trigger events are real and recent — not hallucinated or outdated
- [ ] Pain point hypotheses reflect what we actually know, not generic assumptions
- [ ] Competitive claims match current positioning in `competitive.md`
- [ ] ROI anchor is approved for external use (check `proof.md` source notes)
- [ ] Suggested opening sounds like the rep, not a template

**Time required for review: 10–15 minutes.** If it's taking longer, the brief quality is insufficient — flag the output and rerun Step 1 with more specific account context.

---

## What the rep does with it

The brief is preparation material, not a script. The rep reads it, internalizes what matters, and shows up to the conversation as a person — not someone reading from a document.

The discovery questions are hypotheses, not a checklist. The rep uses them as mental anchors, not a linear sequence. If the conversation goes somewhere unexpected and more valuable, they follow it.

The suggested opening is a starting point. The rep rewrites it in their own voice before the call.

This is the human's lane: taking prepared intelligence and applying it with judgment, presence, and adaptability. The brief gets them to the starting line faster. What happens after that is the rep's craft.

---

## See it in practice

A fully completed brief — built for a specific fictional account scenario — is in:

`/worked-examples/meridian-gtm/presale-brief-example.md`

Read the example before building your first real brief. It shows what "complete" looks like and gives you a quality bar to work against.

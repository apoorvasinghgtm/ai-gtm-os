# Messaging Brief Workflow

**Purpose:** Generate a structured messaging brief for a new segment, product launch, campaign, or GTM motion. Produces a hierarchy of messages — from positioning through to copy — that the whole GTM team can work from.

**Context files required:** All six — `01-company-context.md`, `02-icp-definition.md`, `03-persona-cards.md`, `04-competitive-positioning.md`, `05-proof-library.md`, `06-voice-and-tone.md`

**Time to run:** 20–30 minutes (AI execution) + 30–60 minutes (PMM/GTM lead review and edit)

**When to use:**
- Launching a new product, feature, or pricing tier
- Entering a new vertical or segment
- Refreshing positioning after a competitive shift or rebrand
- Aligning GTM teams before a major campaign

**Who reviews:** PMM or GTM lead must review and approve before distributing. This is a first draft, not a final document.

---

## What You Need Before Running

- **Brief subject:** What exactly are you messaging? [e.g., New product launch — AI call coaching module / New vertical — financial services / Competitive repositioning against Competitor X]
- **Target segment:** Which ICP or sub-segment is this brief for? [Primary ICP / Secondary ICP / New segment — describe]
- **Primary persona:** Who is the most important buyer for this brief? [Title from persona cards]
- **The core problem we're solving:** In one sentence, what problem does this product/launch/campaign address?
- **What's new or different:** What changed that makes this launch worth a messaging refresh? [New capability, new proof, new competitive context, new market timing]
- **Distribution:** Where will this messaging be used? [Sales outreach / Product marketing / Paid campaigns / Event / All of the above]

---

## The Prompt: Full Messaging Brief

**Copy and paste into your Claude Project. Fill in all bracketed fields.**

---

```
Using the context files loaded in this project, generate a messaging brief for the following.

Brief subject: [What you're messaging — product, launch, campaign, segment]
Target segment: [ICP or sub-segment — reference our ICP definition]
Primary persona: [Title of the primary buyer]
Supporting personas: [Other buyers or influencers in this motion]
Core problem we're solving: [One sentence]
What's new or different: [What changed — new capability, new proof, new competitive context]
Distribution channels: [Where this messaging will be used]

Generate a full messaging brief with the following structure:

1. POSITIONING STATEMENT (one paragraph, internal use)
Complete this framework: "For [target customer] who [has this problem], [our product] is [category] that [key benefit]. Unlike [alternative], we [key differentiator]."
Then explain in 2–3 sentences why this positioning is defensible and what proof supports it.

2. VALUE PROPOSITION BY PERSONA
For each persona listed above, write:
- The headline value prop (one sentence, in their language)
- The top three supporting proof points from our proof library
- The key objection they'll have and how the messaging preempts it

3. MESSAGE HIERARCHY (three levels)
- Level 1 — Core message: The single most important thing to communicate. If they remember one thing, it's this.
- Level 2 — Supporting messages (3 messages): The three claims that make the core message credible and specific.
- Level 3 — Proof and evidence (for each supporting message): The specific proof point, stat, or example that substantiates it.

4. COMPETITIVE DIFFERENTIATION NARRATIVE
A two to three sentence narrative that positions us against the most likely alternative (from our competitive positioning file). This should be suitable for a rep to say in a call, not a formal document.

5. COPY BUILDING BLOCKS
Write the following, all consistent with the hierarchy above:
- Headline (under 10 words): The big claim
- Sub-headline (under 25 words): What it means and for whom
- Email subject line (3 options): Direct / Curiosity / Persona-specific
- LinkedIn post opening line: The hook that makes someone stop scrolling
- One-paragraph product description (75 words): For sales decks and one-pagers
- One-line product description (under 20 words): For email signatures, ads, and quick intros

6. WHAT THIS MESSAGING IS NOT
Two to three things this brief explicitly does not claim or promise — important guardrails for teams using it.

7. OPEN QUESTIONS FOR PMM REVIEW
What assumptions are baked into this brief that should be validated before distributing? Flag any place where the context files were unclear or where you made an inference.
```

---

## After the Brief: Stakeholder Alignment Prompt

When you need to share the brief with a cross-functional team and align on it quickly.

---

```
I have a messaging brief for [subject]. Before I distribute it to the GTM team, help me prepare for the review conversation.

Brief: [Paste the messaging brief above]

Generate:
1. A 3-bullet exec summary for the brief — what we decided, why, and what it means for GTM
2. The two or three likely points of disagreement and how to frame each as a decision, not a debate
3. The questions I should ask the team to pressure-test the brief before distributing
4. What I need from sales, product, and CS respectively to make this brief work in the field
```

---

**Quality gate before distributing:**
- [ ] Positioning statement is differentiated and defensible — not generic
- [ ] Every proof point in the brief exists in `05-proof-library.md` and is approved
- [ ] No forbidden language from `06-voice-and-tone.md`
- [ ] Messaging reviewed by at least one sales rep who has had the conversations this brief describes
- [ ] Competitive claims reviewed against `04-competitive-positioning.md`
- [ ] Version number, owner, and date recorded at the bottom of the distributed brief

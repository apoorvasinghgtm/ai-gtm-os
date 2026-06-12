# Competitive Battlecard Workflow

**Purpose:** Generate a one-page competitive battlecard for a specific competitor — designed for reps to use in live deals, not for external distribution.

**Context files required:** `01-company-context.md`, `03-persona-cards.md`, `04-competitive-positioning.md`, `05-proof-library.md`

**Time to run:** 10–15 minutes (AI execution) + 20–30 minutes (PMM review — required before distribution)

**When to use:**
- Before a deal where a specific competitor is in the evaluation
- When a new competitor enters the market
- When a competitor makes a significant product or pricing move
- Quarterly refresh of existing battlecards

**Who reviews:** PMM or product marketing must review every battlecard before it goes to reps. Competitive claims require sign-off.

---

## What You Need Before Running

- **Competitor name:** [Which competitor]
- **Deal context (if applicable):** [What stage is the deal, what has the prospect said about this competitor]
- **Recent competitive developments:** [Any recent moves by this competitor — new features, pricing changes, new customers, funding, executive changes]
- **Your latest wins and losses against this competitor:** [Brief summary — what pattern explains when you win vs. lose]

---

## The Prompt: Full Battlecard

**Copy and paste into your Claude Project. Fill in all bracketed fields.**

---

```
Using the context files loaded in this project, generate a competitive battlecard for use by sales reps in live deals.

Competitor: [Competitor name]
Recent competitive developments: [What's changed recently, or "No recent developments known"]
Deal pattern against this competitor: [When we win vs. lose, if known]
Specific deal context (if applicable): [Prospect name, deal stage, what they've said about this competitor]

Generate a battlecard in the following format. This is for internal rep use — it should be direct, specific, and honest. Not a marketing document.

---

BATTLECARD: [Competitor Name] vs. [Our Company Name]
Last updated: [Today's date]
Owner: [PMM — leave as placeholder]

THE ONE-LINE SUMMARY
[Complete this: "When [Competitor] comes up in a deal, our move is to..."]

WHERE THEY'RE STRONG (be honest — reps need to know this)
- [Strength 1]: [What they do well and why prospects like it]
- [Strength 2]: [Strength and context]
- [Strength 3]: [Strength and context]

WHERE WE WIN
- [Our advantage 1]: [What we do better and the proof — reference our proof library]
- [Our advantage 2]: [Advantage and proof]
- [Our advantage 3]: [Advantage and proof]

WHAT PROSPECTS SAY ABOUT THEM (in their words)
- "[Phrase or observation prospects use when they've evaluated this competitor]"
- "[Another common phrase]"

HOW TO POSITION WHEN THEY'RE IN THE DEAL
- If the prospect mentions them unprompted: [What to say]
- If the prospect is actively evaluating them: [What to say]
- If the prospect is already using them: [What to say — can we complement, or is this a displacement?]

THE THREE QUESTIONS TO ASK
Discovery questions that help you understand how serious the competitive threat is and where you stand:
1. [Question 1 — understand what they've seen from the competitor]
2. [Question 2 — understand what they liked or didn't like]
3. [Question 3 — understand their decision criteria in a way that favors your strengths]

TRAPS TO AVOID
- [Thing NOT to say or do when this competitor comes up — explain why]
- [Another trap]

THE PROOF POINT TO LEAD WITH
[The single best proof point from our proof library for deals where this competitor is present — and when/how to introduce it]

WHAT TO DO IF YOU'RE LOSING TO THEM
[The play when a deal is trending toward the competitor — what to change, who to bring in, what to ask]

---

After generating the battlecard, list any places where the competitive positioning file was unclear or where you made inferences that PMM should verify before distributing.
```

---

## After a Competitive Win or Loss: Debrief Prompt

Use this after any deal where this competitor was involved — win or loss. The output feeds back into your competitive positioning file.

---

```
I just [won / lost] a deal where [Competitor] was involved. Help me capture what I learned.

Deal summary: [Brief — company, ACV, personas involved, deal length]
What happened: [Narrative of how the competitive dynamic played out]
Final decision: [Who won and why — in the buyer's words if you know them]

Based on our battlecard and competitive positioning file, generate:

1. PATTERN UPDATE
What does this deal confirm or challenge in our current battlecard? What should change?

2. NEW INTELLIGENCE
Anything we learned about this competitor — pricing, messaging, product, sales tactics — that isn't in our current positioning file.

3. WHAT WORKED
The one or two moves that helped us (or would have helped us) in this deal.

4. RECOMMENDED BATTLECARD UPDATE
Specific changes to make to the battlecard based on this deal. Flag the section and the suggested edit.
```

---

**Quality gate before distributing to reps:**
- [ ] All competitive strengths listed are honest — not minimized
- [ ] Every claim about our advantages is backed by a proof point from `05-proof-library.md`
- [ ] No claims that aren't in `04-competitive-positioning.md` approved claims section
- [ ] Version number, owner, and date on the document
- [ ] At least one rep who works competitive deals reviewed the battlecard before distribution
- [ ] PMM has signed off on competitive claims

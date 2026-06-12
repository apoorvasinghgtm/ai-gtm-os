# Expansion Intelligence Workflow

**Purpose:** Generate a structured expansion brief for an existing customer — identifying the right expansion play, the timing, the stakeholders, and the messaging — before a QBR, renewal conversation, or upsell motion.

**Context files required:** `01-company-context.md`, `02-icp-definition.md`, `03-persona-cards.md`, `05-proof-library.md`

**Time to run:** 15 minutes (AI execution) + 15 minutes (CSM or AE review)

**When to use:**
- Before a QBR or Executive Business Review
- When a customer is approaching renewal (90 days out)
- When a customer shows expansion signals (new hires, new use cases, inbound questions)
- When a customer champion changes roles or a new stakeholder joins

---

## What You Need Before Running

- **Customer name**
- **Current contract:** ACV, products/modules purchased, contract end date
- **Health score or status:** [Green / Yellow / Red, and why]
- **Champion:** [Name, title]
- **Economic buyer:** [Name, title — same as champion or different?]
- **Usage signals:** [Are they using the product? What do you know about adoption levels?]
- **Expansion trigger:** [What's prompting this conversation — renewal, new team, new use case, QBR, proactive]
- **Outcomes they've achieved:** [What results have they gotten — use specific numbers if you have them]
- **Open issues or risks:** [Anything unresolved — support tickets, dissatisfaction, competitive threats]

---

## The Prompt: Expansion Brief

**Copy and paste into your Claude Project. Fill in all bracketed fields.**

---

```
Using the context files loaded in this project, generate an expansion brief for an existing customer.

Customer: [Company name]
Current ACV: [$amount]
Products purchased: [What they currently use]
Contract end date: [Date]
Health status: [Green / Yellow / Red] — [Why]

Champion: [Name, Title]
Economic buyer: [Name, Title] — [Same as champion or different]
Usage: [What you know about how they're using the product — active / partial / low adoption]
Outcomes achieved: [Results they've gotten — be specific, e.g., "Ramp time down 30% in their last cohort"]
Open issues: [Anything unresolved, or "None known"]
Expansion trigger: [What's prompting this — renewal, new headcount, new use case, QBR, proactive outreach]

Generate the following:

1. EXPANSION OPPORTUNITY ASSESSMENT
What's the most logical expansion play for this customer?
- Cross-sell (new product or module)
- Upsell (larger tier, more seats, more usage)
- Land and expand (new team or department)
- Renewal with commitment increase
Explain the rationale based on their current state and what you know about their business.

2. TIMING ASSESSMENT
Is now the right time to have an expansion conversation? Assess:
- Health status (are they in a good place to expand?)
- Relationship stability (do they trust us enough for this conversation?)
- Business signals (is there a trigger that makes expansion timely?)
If timing is poor, state what needs to happen first and suggest when to revisit.

3. EXPANSION NARRATIVE
The story to tell in the expansion conversation — grounded in their outcomes, not our product features.
Format: "You've achieved [X]. The next opportunity is [Y]. Here's what that looks like for a customer at your stage..."
Pull from our proof library for relevant examples of customers who expanded and what they gained.

4. STAKEHOLDER APPROACH
- Who to bring the expansion conversation to first (champion or economic buyer?)
- What each stakeholder needs to hear to support the expansion
- Who else needs to be involved (new department heads, IT, legal for contract changes?)

5. QBR AGENDA (if this brief is for a QBR)
A proposed agenda:
- Opening: How to frame the business review to set up the expansion conversation
- Results review: How to present their outcomes in a way that builds the case
- Future state: How to introduce the expansion without it feeling like a sales pitch
- Close: What you want them to commit to by end of the QBR

6. RISKS TO THE EXPANSION
What could make this expansion fail or stall? For each risk, note how to preempt or address it.

7. THE ASK
Be specific: What exactly are you asking this customer to do, commit to, or approve? When do you need a decision?
```

---

## Customer Health Check: At-Risk Account

Use this when a customer is yellow or red and you need to stabilize before any expansion conversation is appropriate.

---

```
One of my customers is at risk. I need to stabilize this account before thinking about renewal or expansion.

Customer: [Company name]
Current ACV: [$amount]
Health status: [Yellow / Red]
Why they're at risk: [Be specific — low adoption, support issues, champion left, competitor entered, dissatisfaction with specific feature or outcome]
What we've done so far: [Steps already taken]
Their current sentiment: [What they've said — frustrated, patient, disengaged, etc.]
Key upcoming touchpoint: [Next call, QBR, or renewal date]

Using our context files, generate:
1. Root cause assessment — what's most likely driving the risk
2. Immediate actions to take in the next two weeks
3. The message to send to the champion this week — honest, not defensive
4. If the champion is gone: how to re-establish a relationship with the new contact
5. What success looks like at 30 / 60 / 90 days to get this account back to green
6. When and how to reintroduce the expansion conversation (if at all)
```

---

**Quality gate before a QBR or renewal conversation:**
- [ ] You have at least one confirmed outcome this customer has achieved — with numbers
- [ ] You know the health status and the reason behind it
- [ ] You know who the economic buyer is and whether they'll be in the room
- [ ] You've cleared the expansion proof point for use with this customer
- [ ] You have a specific ask ready — not "let's discuss options"

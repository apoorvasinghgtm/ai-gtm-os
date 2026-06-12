# Deal Inspection Workflow

**Purpose:** Generate a structured deal inspection for an open opportunity — identifying what's real, what's at risk, what's missing, and what to do next. Designed for use by sales managers in pipeline reviews and by reps preparing for forecast calls.

**Context files required:** `01-company-context.md`, `02-icp-definition.md`, `03-persona-cards.md`, `04-competitive-positioning.md`

**Time to run:** 10 minutes (AI execution) + 15 minutes (manager or rep review)

**When to use:**
- Weekly pipeline reviews with sales managers
- Before a forecast call
- When a deal stalls or goes silent
- Before committing a deal to the forecast

---

## What You Need Before Running

Gather the following from your CRM before running:

- **Account name and deal name**
- **ACV and deal stage**
- **Expected close date**
- **Days in current stage**
- **Economic buyer:** [Name, title — confirmed or assumed?]
- **Champion:** [Name, title — do they have access to budget?]
- **Technical evaluator / other stakeholders:** [Names and roles]
- **Last meaningful activity:** [What happened and when — not just "email sent"]
- **Next committed step:** [What the prospect has committed to, with a date]
- **Competition in the deal:** [Competitors identified, or "unknown"]
- **Why they'd buy:** [What pain or outcome is driving this — what they've said]
- **Why they might not:** [What's uncertain, unresolved, or at risk]

---

## The Prompt: Deal Inspection

**Copy and paste into your Claude Project. Fill in all bracketed fields.**

---

```
Using the context files loaded in this project, run a structured deal inspection for the following opportunity.

Account: [Company name]
Deal: [Deal name or description]
ACV: [$amount]
Stage: [Stage name]
Expected close: [Date]
Days in current stage: [Number]

Economic buyer: [Name, Title] — [Confirmed in conversation / Assumed based on title / Unknown]
Champion: [Name, Title] — [Has budget access: Yes / No / Unknown]
Other stakeholders: [Names and roles, or "Not mapped"]

Last meaningful activity: [What happened, when]
Next committed step: [What the prospect has committed to, and by when — or "None committed"]

Competition: [Competitor names, or "Unknown / Status quo"]
Why they'd buy: [What they've told you is driving this decision]
Why they might not: [Your honest concerns about this deal]

Run this inspection:

1. DEAL HEALTH ASSESSMENT
Score this deal: Strong / Qualified / At Risk / Stalled
Give a 2–3 sentence rationale for your score based on the information above.

2. WHAT'S REAL AND WHAT'S ASSUMED
For each of the following, tell me whether it's confirmed (they've said it) or assumed (I inferred it):
- The economic buyer is identified and engaged
- The champion has access to budget
- There is a compelling event or deadline
- The close date is real (not wishful)
- We understand the decision criteria
Flag the most dangerous assumption in this deal.

3. THE CRITICAL UNKNOWN
The single most important thing you don't know yet that would change your assessment of this deal. What's the question to ask in the next interaction?

4. RISK FACTORS
Identify which of the following apply to this deal and explain why:
- No executive sponsor engaged
- Champion lacks budget authority
- Competitor is actively in the deal
- Close date has slipped before
- No committed next step from the prospect
- Stalled in this stage longer than typical (reference our ICP's typical deal length)

5. RECOMMENDED ACTIONS (specific, not generic)
Three concrete actions to take before the next forecast call, with the rationale for each. State who does what and by when.

6. FORECAST RECOMMENDATION
Should this deal be included in the forecast for [close month]?
- Commit: High confidence based on evidence
- Upside: Possible but not certain — specify what has to happen
- Pipeline: Too early or too uncertain — keep moving but don't commit
Explain in 2 sentences.
```

---

## Pipeline Review Pack: Multiple Deals

For a manager reviewing multiple deals before a pipeline call, use this to inspect a batch.

---

```
I need to review my pipeline before a forecast call. Here are my open deals:

[For each deal, paste a brief summary: Account, ACV, Stage, Close Date, Last Activity, Next Step]

Using our ICP definition and typical deal dynamics from our context files, generate:

1. A one-line health assessment for each deal (Strong / At Risk / Stalled / Needs attention)
2. The deal I should be most worried about and why
3. The deal I'm most likely underinvesting in — where I have more upside than I'm treating it
4. The one question I need to get answered across the most deals this week
5. A proposed agenda for the pipeline review call — what to spend time on and in what order
```

---

**Quality gate before a forecast call:**
- [ ] Economic buyer is confirmed, not assumed
- [ ] You have a next committed step with a date from the prospect side
- [ ] You know who else is evaluating (competition and internal stakeholders)
- [ ] Close date reflects a real deadline, not your internal target
- [ ] You've had a conversation that confirms budget in the last 30 days

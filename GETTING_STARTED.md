# Getting Started with the AI GTM OS

This guide is for anyone who wants to use this system — not just read about it.

It tells you exactly where to start based on your situation, what to build first, and what "ready to use" looks like at each stage.

---

## Before you start: one decision

**Are you setting this up for yourself, or for a team?**

The system works for both. But the starting point is different.

- **Individual:** You're a PMM, GTM lead, or consultant who wants AI-assisted workflows for your own work. Start at [Step 1 — Build your context layer](#step-1--build-your-context-layer).
- **Team lead:** You're setting this up for a sales, enablement, or marketing team. Read [Operationalizing for Teams](../06-operationalizing-for-teams/from-individual-to-team.md) first — it explains the architecture decisions you need to make before building anything. Then come back here.

---

## What you need before you start

- Access to an AI tool: Claude (recommended), ChatGPT, or equivalent
- 2–3 hours for the initial context layer build
- Basic knowledge of your company's ICP, positioning, and competitive landscape
- For teams: alignment from a VP or senior leader that this will be the standard, not an optional resource

You do not need coding skills. You do not need to set up integrations. Every workflow in this system runs in a standard AI chat interface.

---

## Step 1 — Build your context layer

**Time required:** 2–3 hours
**File to follow:** [`01-foundation/context-layer-setup.md`](../01-foundation/context-layer-setup.md)

This is the foundation everything else runs on. Do not skip it or rush it.

The context layer is six documents:

| Document | What it contains | Time to build |
|---|---|---|
| `company.md` | What you sell, how it works, differentiators, what you are not | 30 min |
| `icp.md` | Firmographics, technographics, trigger signals, negative ICP | 30 min |
| `personas.md` | 3–4 buyer persona cards with goals, pain points, objection patterns | 45 min |
| `competitive.md` | Top 3 competitors: where you win, where you lose, how to position | 30 min |
| `proof.md` | Metrics, customer quotes, proof points organized by persona and outcome | 20 min |
| `voice.md` | Tone rules, approved terminology, what to never say | 15 min |

**Reference:** The Meridian GTM worked example has fully populated versions of all six documents. Use them as a quality benchmark — your documents should be at least as specific.
→ [`worked-examples/meridian-gtm/company-context.md`](../worked-examples/meridian-gtm/company-context.md)
→ [`worked-examples/meridian-gtm/icp-and-personas.md`](../worked-examples/meridian-gtm/icp-and-personas.md)

**How to build them:** Open your AI tool. For each document, use this prompt:

```
I need to build a [company / ICP / persona / competitive / proof / voice] 
document for my GTM context layer.

Here's what I know: [paste everything you know about this topic]

Use the template structure from the AI GTM OS and help me fill it in completely. 
Push back where my answers are too vague — I need specific, usable content, 
not placeholder text.
```

Work through each document in order. The later ones get easier because each builds on the previous.

**You're done with Step 1 when:** All six documents are complete, specific, and you'd be comfortable handing them to a new hire as their onboarding reference.

---

## Step 2 — Run your first workflow

**Time required:** 30–45 minutes to set up, 15 minutes per use after that
**File to follow:** [`02-presale-intelligence/account-research-workflow.md`](../02-presale-intelligence/account-research-workflow.md)

The pre-sale intelligence workflow is the highest-value starting point for most GTM teams. It produces the most immediate, visible time savings — and it's the easiest workflow to quality-check because you know the account.

**How to run it for the first time:**

1. Open [`02-presale-intelligence/account-research-workflow.md`](../02-presale-intelligence/account-research-workflow.md) and read the full workflow before running anything
2. Pick a real account you have a meeting with in the next 5 days
3. Open your AI tool in a new session
4. Paste your context layer documents (company.md, icp.md, personas.md, competitive.md, proof.md) into the session first
5. Run Step 1 of the prompt chain with your account details
6. Review the output, then run Step 2, then Step 3
7. Read the finished brief against the review gate checklist before using it

**Reference:** A fully completed brief is in [`worked-examples/meridian-gtm/presale-brief-example.md`](../worked-examples/meridian-gtm/presale-brief-example.md). Read it before your first run so you know what "complete" looks like. The inline annotations explain why each section was written the way it was.

**You're done with Step 2 when:** You've run the workflow on a real account, reviewed the output against the checklist, and used the brief in an actual meeting.

---

## Step 3 — Understand the human vs. AI boundary

**Time required:** 20 minutes to read, ongoing to apply
**File to follow:** [`01-foundation/human-vs-ai-responsibility.md`](../01-foundation/human-vs-ai-responsibility.md)

Before you add more workflows, read this document. It defines what AI produces and what humans decide across every workflow in this system.

This is not optional background reading. It is the design principle that determines whether the system makes you better or just faster. Fast and wrong is worse than slow and right.

**The question to ask about every workflow you add:** What is the human doing at the review gate, and what decision are they making? If the answer is "checking that it looks okay," the review gate is not doing its job.

---

## Step 4 — Set up prompt governance (teams only)

**Time required:** 1 hour to set up, low ongoing overhead
**File to follow:** [`01-foundation/prompt-governance.md`](../01-foundation/prompt-governance.md)

If you're running this as an individual, skip this step for now.

If you're setting this up for a team, do this before you share any workflows with anyone. The governance structure — version control, named owners, feedback loop — is what prevents the system from degrading silently after the first month.

Minimum viable governance for a small team (under 10 people):
- One owner per workflow prompt
- A shared folder where all context documents live and are accessible to everyone
- A Slack channel or equivalent for flagging bad outputs
- A calendar reminder for monthly review

---

## Step 5 — Adapt the worked examples to your company

**Time required:** 2–3 hours per vertical
**Files to reference:** [`worked-examples/`](../worked-examples/)

Two fully built examples are included:

- **Meridian GTM** — RevTech, AI Sales Intelligence, sales-led enterprise motion
- **TalentFlow AI** — HRTech, AI Sourcing & Screening, hybrid PLG + sales-led motion

These are not templates to fill in. They are reference implementations — showing what the full system looks like when it's working correctly for a specific company and GTM motion.

Use them to calibrate the quality and specificity of your own context layer and workflows. If your documents are less specific than these, they will produce less useful outputs.

---

## Quick reference: file map

| What you want to do | Where to go |
|---|---|
| Build your context layer | [`01-foundation/context-layer-setup.md`](../01-foundation/context-layer-setup.md) |
| Run pre-sale account research | [`02-presale-intelligence/account-research-workflow.md`](../02-presale-intelligence/account-research-workflow.md) |
| See a completed brief example | [`worked-examples/meridian-gtm/presale-brief-example.md`](../worked-examples/meridian-gtm/presale-brief-example.md) |
| Understand what AI owns vs. humans | [`01-foundation/human-vs-ai-responsibility.md`](../01-foundation/human-vs-ai-responsibility.md) |
| Set up governance for a team | [`01-foundation/prompt-governance.md`](../01-foundation/prompt-governance.md) |
| Operationalize across a team | [`06-operationalizing-for-teams/from-individual-to-team.md`](../06-operationalizing-for-teams/from-individual-to-team.md) |
| See a full vertical example (RevTech) | [`worked-examples/meridian-gtm/`](../worked-examples/meridian-gtm/) |
| See a full vertical example (HRTech) | [`worked-examples/talentflow-ai/`](../worked-examples/talentflow-ai/) |

---

## Common mistakes to avoid

**Building workflows before the context layer is complete.**
Every workflow runs on top of the context layer. A weak context layer produces weak outputs regardless of how well the prompt is written. Build the foundation first.

**Skipping the review gate.**
The review gate is not optional overhead. It is the mechanism that makes AI outputs trustworthy. A rep who uses an unreviewed brief in a customer meeting and gets something wrong has not saved time — they've created a trust problem.

**Treating the worked examples as fill-in-the-blank templates.**
The worked examples are specific by design. Generic inputs produce generic outputs. The goal is to build your own context layer that is equally specific to your company, your buyers, and your GTM motion.

**Setting this up for a team without an assigned owner.**
Systems without owners degrade. Before you share this with anyone, name the person responsible for maintaining the context layer and governing the prompt library. If that person doesn't exist yet, you're not ready to scale.

---

## Questions or feedback

This is a living system. If something doesn't work as described, or if you've adapted it for a use case not covered here, open an issue or reach out directly.

→ [LinkedIn](https://www.linkedin.com/in/apoorvasingh1/)
→ [Substack](https://apoorvasplaybook.substack.com/)

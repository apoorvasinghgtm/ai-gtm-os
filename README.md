# AI GTM OS

An open-source operating system for AI-native go-to-market and product marketing teams.

Built by [Apoorva Singh](https://www.linkedin.com/in/apoorvasingh1/) — AI GTM and product marketing leader with 14+ years launching AI products at Indeed, Google, and Expedia. $75M+ ARR generated from AI product launches across 28 markets.

---

## What This Is

Most teams use AI for one-off tasks. This system makes AI a permanent, reliable part of how your GTM team operates — with consistent outputs, shared context, and clear human review gates.

The AI GTM OS gives you:
- **A context layer** — the foundation that makes every AI output specific to your company, not generic
- **Pre-built workflows** — copy-paste prompt chains for the work GTM teams do every week
- **Governance frameworks** — version control, ownership, and feedback loops to keep the system reliable at team scale
- **Worked examples** — complete outputs across two verticals (RevTech and HRTech) to calibrate against

---

## How to Get Started in Under an Hour

**The fastest path to running your first workflow:**

1. Fork or download this repository
2. Open `_templates/context/` and fill in `01-company-context.md` (45–60 min)
3. Read `claude-projects-setup.md` — create a Claude Project and upload your context file
4. Run Step 1 of `02-presale-intelligence/account-research-workflow.md` on a real account

You'll have your first AI-generated pre-sale brief in under 2 hours from a standing start.

For the full system: see `GETTING_STARTED.md` for the complete implementation path.

---

## Repository Structure

```
ai-gtm-os/
│
├── _templates/                        ← START HERE
│   ├── README.md                      ← How to use the templates
│   └── context/
│       ├── 01-company-context.md      ← Your product, model, differentiators, proof points
│       ├── 02-icp-definition.md       ← Ideal customer profile, fit signals, negative ICP
│       ├── 03-persona-cards.md        ← Buyer personas: goals, pains, objections, language
│       ├── 04-competitive-positioning.md  ← Competitors, where you win/lose, displacement strategy
│       ├── 05-proof-library.md        ← Approved metrics and quotes indexed by outcome and persona
│       └── 06-voice-and-tone.md       ← Writing rules, forbidden language, before/after examples
│
├── claude-projects-setup.md           ← Step-by-step: upload context, configure Claude Projects, test
│
├── 01-foundation/
│   ├── context-layer-setup.md         ← Why the context layer matters and how to build it right
│   ├── human-vs-ai-responsibility.md  ← What AI owns vs. what humans own in GTM workflows
│   └── prompt-governance.md          ← Versioning, ownership, and feedback loops for teams
│
├── 02-presale-intelligence/
│   └── account-research-workflow.md  ← 3-step prompt chain: situation → hypotheses → call prep
│
├── 03-sales-motion/
│   ├── discovery-call-prep.md        ← Call plan, question arc, multi-stakeholder navigation
│   └── outbound-personalization.md   ← Single email, 3-touch sequence, LinkedIn, response handling
│
├── 04-enablement-architecture/
│   ├── messaging-brief.md            ← Positioning, message hierarchy, copy building blocks
│   └── competitive-battlecard.md     ← Rep-ready battlecard for live competitive deals
│
├── 05-pipeline-and-expansion/
│   ├── deal-inspection.md            ← Pipeline review, forecast qualification, risk flags
│   └── expansion-intelligence.md    ← QBR prep, expansion brief, at-risk account recovery
│
├── 06-operationalizing-for-teams/
│   └── from-individual-to-team.md    ← How to scale from one person to a full GTM org
│
└── worked-examples/
    ├── meridian-gtm/                 ← RevTech vertical (sales intelligence platform)
    │   ├── company-context.md
    │   ├── icp-and-personas.md
    │   └── presale-brief-example.md
    └── talentflow-ai/               ← HRTech vertical (AI sourcing and screening)
        ├── company-context.md
        ├── icp-and-personas.md
        └── presale-brief-example.md
```

---

## Workflows at a Glance

| Workflow | What It Produces | Who Uses It | Time |
|----------|-----------------|-------------|------|
| Pre-sale intelligence | Account brief before a discovery call | AE, SDR | 15–20 min AI + 15 min review |
| Discovery call prep | Question arc, hypothesis, call structure | AE | 10 min AI + 10 min review |
| Outbound personalization | Email/LinkedIn sequence for specific accounts | SDR, AE | 10 min AI + 5 min edit |
| Messaging brief | Positioning, hierarchy, copy blocks for launches | PMM, GTM lead | 20–30 min AI + 30–60 min PMM review |
| Competitive battlecard | Rep-ready card for live competitive deals | PMM, AE | 10–15 min AI + 20–30 min PMM review |
| Deal inspection | Pipeline health, risk flags, forecast guidance | AE, Sales manager | 10 min AI + 15 min review |
| Expansion intelligence | QBR prep, expansion narrative, at-risk recovery | CSM, AE | 15 min AI + 15 min review |

---

## Who This Is For

**Individual practitioners** — GTM strategists, PMMs, AEs, CSMs, and SDRs who want AI to do the research-intensive, repeatable work so they can focus on judgment, relationships, and strategy.

**Cross-functional GTM teams** — Sales, marketing, CS, and RevOps teams who want consistent AI outputs across functions, not different prompts on different laptops.

**GTM leaders** — VPs and directors building scalable GTM infrastructure, not just individual productivity hacks.

---

## The Design Principles

**Context before workflows.** Generic AI produces generic outputs. Everything in this system is designed to run against your specific context layer — your product, your ICP, your personas, your proof points, your voice. Build the context layer first.

**Humans own judgment.** AI owns research, synthesis, and first drafts. Humans own live conversations, strategic decisions, and anything that requires relationship or creativity. Every workflow has explicit human review gates.

**Governance makes it durable.** A system that works for one person once isn't a system. The governance layer — versioning, ownership, feedback loops — is what makes this reliable at team scale over time.

---

## Worked Examples

See `/worked-examples/` for complete implementations across two verticals:

- **Meridian GTM** — RevTech: AI-powered sales intelligence platform. Enterprise B2B SaaS, $80K–$250K ACV.
- **TalentFlow AI** — HRTech: AI-powered sourcing and screening. PLG + sales-led hybrid, $2K–$200K ARR.

Use these to calibrate what "good" looks like before you run workflows on your own accounts.

---

## Building in Public

This system is actively being developed. Feedback, forks, and contributions are welcome.

- **Questions or feedback:** Open an issue
- **Following the build:** [Substack](https://apoorvasplaybook.substack.com) | [LinkedIn](https://linkedin.com/in/apoorvasingh1)
- **Fractional GTM advisory:** [Contact Apoorva](https://linkedin.com/in/apoorvasingh1)

---

*MIT License — free to use, fork, and adapt.*

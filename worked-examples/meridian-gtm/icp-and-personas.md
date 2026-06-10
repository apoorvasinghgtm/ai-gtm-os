# Meridian GTM — ICP & Persona Cards

**Fictional company. Built as a reference example for the AI GTM OS.**

---

## Ideal Customer Profile (ICP)

### Firmographics

| Attribute | Primary ICP | Secondary ICP |
|---|---|---|
| Company size | 500–5,000 employees | 200–500 employees |
| Revenue | $50M–$1B ARR | $20M–$50M ARR |
| Industry | B2B SaaS, FinTech, Enterprise Tech | Professional Services, Manufacturing with complex sales |
| Geography | North America (primary), EMEA (growing) | — |
| Sales team size | 50+ AEs | 20–50 AEs |
| Deal complexity | Multi-stakeholder, 60–180 day cycles | — |
| ACV | $50K+ | $30K–$50K |

### Technographic signals (fit indicators)

**Strong fit:**
- Uses Salesforce or HubSpot as primary CRM
- Has Gong or Chorus deployed (complementary, not competitive)
- Uses a third-party intent data provider (6sense, Bombora, G2)
- LinkedIn Sales Navigator licensed at team or enterprise level
- Outreach or Salesloft in the sales stack

**Poor fit signals:**
- Primarily transactional or PLG motion with no sales team
- Average deal size below $30K ACV
- No dedicated RevOps or Sales Enablement function
- Stack is entirely homegrown or legacy (indicates change-averse org)

### Behavioral / trigger signals (buying readiness)

- VP of Sales or CRO hire in last 90 days (new leader, clean slate)
- Sales team headcount growth >20% in last 6 months (scaling pain)
- "Sales productivity" or "rep ramp time" appearing in job postings or earnings calls
- Recent miss on quota or public commentary about pipeline quality
- Competitive loss rate increasing (visible in Gong call themes if we have access)
- Series B or C funding event in last 6 months (capital to invest, pressure to perform)

### Negative ICP

- Company primarily sells to SMB with high-velocity, transactional motion
- Sales cycle shorter than 30 days (Meridian's value doesn't compound in this context)
- No sales ops or enablement function to drive adoption
- Currently in a hiring freeze affecting GTM roles
- Recently acquired — GTM stack in flux, decision-making stalled

---

## Persona Cards

---

### Persona 1: VP of Sales / CRO
**Role in deal:** Economic buyer. Signs the contract. Often the initiating champion in larger deals.

**Goals:**
1. Hit quota consistently — not just this quarter, but predictably across the team
2. Reduce rep ramp time to <90 days and increase ramp-to-productivity ratio
3. Improve win rates on competitive deals without adding headcount

**Pain points (in their language):**
1. "My reps spend half their time on research and prep instead of selling."
2. "We're losing deals we should win because our reps walk in underprepared."
3. "I can't tell which deals are actually healthy until it's too late to save them."

**How they evaluate:**
- Wants to see proof from companies at their stage and motion — not generic case studies
- Will ask for pilot data before full commit; needs to see rep adoption, not just exec enthusiasm
- ROI justification needs to hold up to CFO scrutiny — build the business case for them
- Talks to peers in their network before deciding; reference customers matter more than demos

**Language to use:** Pipeline efficiency, rep productivity, ramp velocity, win rate, revenue per rep

**Language to avoid:** "AI-powered," "machine learning," "data-driven" (overused, triggers skepticism) — show, don't claim

**Objection patterns:**
1. *"My reps won't use another tool"* → Root cause: Past tool fatigue from failed implementations. Address with stack-native integration story and adoption data from similar orgs.
2. *"We already have Gong and Sales Navigator"* → Root cause: Doesn't understand the synthesis layer. Gong records and transcribes; Navigator finds contacts; Meridian combines signals and produces the brief. They're inputs, not substitutes.
3. *"Show me the ROI"* → Root cause: Genuine need for CFO-ready justification, not skepticism. Use the pre-built ROI model with their industry benchmarks. Offer to run the model live with their numbers.

---

### Persona 2: Head of Sales Enablement / Revenue Enablement
**Role in deal:** Champion. Closest to the day-to-day pain. Often the internal sponsor who builds the business case and drives adoption.

**Goals:**
1. Reduce time reps spend on non-selling activities
2. Build a scalable onboarding program that doesn't depend on tribal knowledge
3. Demonstrate measurable impact of enablement programs to CRO

**Pain points (in their language):**
1. "I build content and playbooks that nobody uses because they're too generic."
2. "New reps take 6+ months to ramp — we lose them before they're productive."
3. "I can't prove the ROI of what I do. It's all anecdotal."

**How they evaluate:**
- Highly practical — wants to see the product, not the pitch
- Cares about rep experience: will the brief actually help a rep, or just create more work?
- Will test it themselves before showing it to the VP
- Interested in the analytics layer — can they see which reps are using it and how?

**Language to use:** Rep experience, time-to-productivity, enablement ROI, adoption rate, content utilization

**Objection patterns:**
1. *"This is interesting but I need VP buy-in to move forward"* → Root cause: Organizational dynamics, not skepticism. Offer to help them build the internal business case and prep the VP presentation.
2. *"How do we ensure the briefs stay accurate as our market changes?"* → Root cause: Past experience with data tools that go stale. Walk through the context layer maintenance protocol and versioning system.

---

### Persona 3: RevOps / Sales Operations Leader
**Role in deal:** Technical evaluator and internal gatekeeper. Has veto power on anything that touches the CRM or data stack.

**Goals:**
1. Maintain data integrity in the CRM — no tools that create shadow systems or dirty data
2. Reduce rep admin time without creating new integration maintenance burden
3. Build reporting infrastructure that gives leadership accurate pipeline visibility

**Pain points (in their language):**
1. "Every new tool creates a new integration I have to maintain."
2. "Reps don't update the CRM so my pipeline data is unreliable."
3. "I spend more time fixing data problems than building systems."

**How they evaluate:**
- Wants the technical integration specs before the business case conversation
- Will ask about data residency, security certifications, and API rate limits
- Concerned about what happens to CRM data quality — does Meridian write to records or read-only?
- Interested in the admin layer: who maintains the context layer, how does it get updated?

**Language to use:** Integration architecture, data hygiene, CRM enrichment, API connectivity, audit trail

**Objection patterns:**
1. *"We have a strict security review process"* → Root cause: Legitimate. Not an objection to navigate around — take it seriously. Provide SOC 2 Type II report, data processing agreement, and offer to connect with Meridian's security team directly.
2. *"This will create another tool reps ignore"* → Root cause: Has seen this before. Show adoption data and the stack-native integration that surfaces briefs inside tools reps already use.

---

### Persona 4: AE / Senior Account Executive (end user)
**Role in deal:** Not a buyer, but a critical influencer. If reps hate it, the VP won't renew.

**Goals:**
1. Walk into every meeting knowing enough to be genuinely useful, not just present
2. Spend time on deals likely to close — not on accounts that aren't ready
3. Build a credible business case without spending a week on financial modeling

**Pain points (in their language):**
1. "I spend Sunday nights doing research I should have had on Friday."
2. "I never know if I'm missing something obvious about an account before I walk in."
3. "Building an ROI model from scratch for every deal takes forever and I'm not a finance person."

**How they evaluate:**
- Purely practical: does this make my job easier or harder?
- Will judge the product in the first 10 minutes — brief quality has to be immediately impressive
- Does not care about integrations, security, or admin — just: is the brief actually useful?

**Language to use:** Prep time, walking in confident, not wasting their time, knowing the account

**What to show them:** A real brief — ideally for an account they know — in the first interaction. Let the product speak.

---

## Deal dynamics

**Typical buying committee:** VP Sales (economic buyer) + Head of Enablement (champion) + RevOps (technical evaluator)

**Common deal patterns:**
- Champion-led: Enablement leader discovers, builds internal case, brings in VP
- Top-down: CRO initiates after peer recommendation, assigns Enablement to evaluate
- RevOps-initiated: Ops leader evaluating stack consolidation, flags as opportunity

**Where deals stall:**
- Stuck in IT/Security review (RevOps gatekeeper concern)
- Champion loses internal sponsorship (VP changes priorities or org restructures)
- ROI model not compelling enough for CFO — usually means we didn't build it with their numbers

**What accelerates deals:**
- Strong reference customer at similar company, similar motion
- Pilot with real accounts that produces a measurable brief quality improvement
- Pre-built ROI model that CFO can approve without modification

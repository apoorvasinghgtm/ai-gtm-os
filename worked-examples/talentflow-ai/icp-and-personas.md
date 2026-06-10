# TalentFlow AI — ICP & Persona Cards

**Fictional company. Built as a reference example for the AI GTM OS.**

---

## How this differs from Meridian GTM

TalentFlow runs a hybrid PLG + sales-led motion. This changes the ICP model: there are two distinct entry points — self-serve (PLG) and sales-led (enterprise) — with different buyer profiles, different trigger signals, and different conversion paths.

The personas below cover the enterprise sales-led motion. PLG buyers are not included here because they self-qualify through product usage; sales intervention is not part of their journey until expansion.

---

## Ideal Customer Profile

### Enterprise ICP (sales-led motion)

| Attribute | Primary ICP | Secondary ICP |
|---|---|---|
| Company size | 1,000–10,000 employees | 500–1,000 employees |
| Open roles at any time | 50+ concurrent | 20–50 concurrent |
| TA team size | 10+ recruiters | 5–10 recruiters |
| Industry | B2B Tech, FinTech, Healthcare Tech, Professional Services | Any knowledge-work-heavy industry with competitive talent markets |
| Geography | North America (primary), UK | ANZ |
| ATS | Greenhouse, Lever, Workday Recruiting | iCIMS, SAP SuccessFactors |
| Hiring velocity | High — consistent volume, not episodic | — |

### Technographic signals (fit indicators)

**Strong fit:**
- Greenhouse or Lever as primary ATS (native integration, fast implementation)
- LinkedIn Recruiter at team or enterprise tier (signals investment in sourcing)
- No existing AI sourcing layer — or a failed one they're replacing
- HR tech stack review underway (budget allocated, decision imminent)

**Poor fit:**
- Workday Recruiting as ATS without IT resources for implementation
- Primarily hourly or frontline hiring (our screening model is optimized for knowledge work roles)
- Highly regulated hiring process with legal constraints on AI-assisted screening (financial services with strict compliance requirements — requires compliance review before engaging)
- TA team of fewer than 5 — ROI doesn't clear the threshold

### Behavioral / trigger signals (buying readiness)

- TA team headcount flat or reduced while hiring volume is increasing (efficiency mandate)
- Recent CHRO or VP of Talent Acquisition hire (new leader, fresh agenda)
- Company in hypergrowth mode post-funding (hiring velocity outpacing recruiter capacity)
- Active job postings for "Recruiting Operations" or "TA Technology" roles (stack investment underway)
- Negative Glassdoor candidate experience reviews citing slow process or lack of communication
- Competitor of theirs known to be using AI sourcing (competitive pressure on talent brand)

### Negative ICP

- Primarily hourly, shift-based, or frontline workforce (wrong screening model)
- Hiring freeze or headcount reduction underway
- Recent AI implementation failure creating org-wide skepticism (requires extended trust-building before any AI vendor can succeed)
- No dedicated TA function — hiring owned by HRBPs without recruiting specialization
- Compliance-heavy regulated industry without dedicated HR legal review capacity

---

## Persona Cards

---

### Persona 1: VP of Talent Acquisition / Head of TA
**Role in deal:** Economic buyer in mid-market. Champion or co-buyer in enterprise (CHRO owns budget at larger orgs).

**Goals:**
1. Scale hiring capacity without proportional headcount increase in TA — do more with the team they have
2. Reduce time-to-hire without compromising quality of hire (these are in tension; they know it)
3. Build a talent acquisition function that's seen as a strategic partner to the business, not a transactional service

**Pain points (in their language):**
1. "My team is drowning in sourcing and scheduling. They don't have time to actually recruit."
2. "We're losing candidates to competitors because our process is too slow."
3. "I can't show the business that TA is a competitive advantage when we're measured on time-to-fill."

**How they evaluate:**
- Wants proof from comparable companies — same industry, similar hiring volume, similar team size
- Deeply skeptical of AI claims — has been burned before by tools that promised automation and delivered noise
- Will ask about candidate experience explicitly: does AI screening feel impersonal or off-putting to candidates?
- Needs to be able to defend the decision to the CHRO and legal — compliance and data privacy questions are not optional

**Language to use:** Recruiter capacity, quality of hire, candidate experience, time-to-hire, TA as strategic function

**Language to avoid:** "Automate your hiring," "AI replaces screening" — will immediately lose credibility

**Objection patterns:**
1. *"We tried AI sourcing before and the candidates were terrible"* → Root cause: Prior tool was keyword-matching, not role-context fit scoring. Differentiate on the fit model specifically — ask what the prior tool was doing and show the contrast.
2. *"What about candidate experience — does this feel robotic?"* → Root cause: Genuine concern, not a negotiating tactic. Lead with the candidate NPS data and the async format research. Offer to share candidate feedback verbatim.
3. *"Our legal team will never approve AI in hiring"* → Root cause: EEOC/OFCCP compliance concern, especially for US enterprise. Have compliance documentation ready. Offer a legal review session with TalentFlow's compliance team.

---

### Persona 2: CHRO / Chief People Officer
**Role in deal:** Economic buyer at enterprise (1,000+ employees). Often not in the evaluation process until final approval.

**Goals:**
1. Build an employer brand that attracts top talent in competitive markets
2. Ensure hiring practices are legally defensible and equitable
3. Demonstrate to the board that people investments are producing measurable business outcomes

**Pain points:**
1. "Talent is our biggest competitive advantage — and our TA process doesn't reflect that."
2. "I'm accountable for pay equity and hiring bias, and I need tools that help, not hurt."
3. "The business wants faster hiring. I want better hiring. These feel like they're in conflict."

**How they evaluate:**
- Does not evaluate tools in detail — evaluates the VP of TA's recommendation and the risk/compliance picture
- Primary concern is reputational and legal risk from AI-assisted hiring decisions
- Wants to understand governance: who is responsible if AI screening produces a biased outcome?
- Will ask about DEI implications explicitly — be prepared with a specific, evidence-based answer

**What to show them:**
- The human-in-the-loop architecture — every decision is a human decision
- Compliance documentation and audit trail capabilities
- Evidence that the tool improves, not degrades, diversity in the qualified slate

---

### Persona 3: Recruiting Operations / TA Technology Manager
**Role in deal:** Technical evaluator. Can be a strong internal champion if they see the integration architecture clearly.

**Goals:**
1. Maintain ATS data integrity — no tools that create shadow systems or duplicate records
2. Reduce the maintenance burden of the HR tech stack — every integration creates ongoing work
3. Enable the recruiting team without becoming their permanent IT support

**Pain points:**
1. "Every tool the TA team wants to add creates three new integrations I have to maintain."
2. "Our ATS data is already a mess. I can't add anything that makes it worse."
3. "Recruiters adopt tools for two weeks and then go back to their spreadsheets."

**How they evaluate:**
- Wants technical specs before the business case conversation
- Will test the ATS integration themselves before recommending to the VP
- Cares deeply about what data TalentFlow writes back to the ATS and what it reads
- Will ask about SSO, data residency, SOC 2 compliance, and GDPR (for EU roles) early

**Language to use:** Integration architecture, ATS writeback, data hygiene, implementation timeline, admin overhead

**Objection patterns:**
1. *"Our Greenhouse admin will need to be involved"* → Root cause: Protecting their domain, appropriately. Welcome this. Offer a dedicated technical session with TalentFlow's implementation team and the Greenhouse admin together.
2. *"How long does implementation take?"* → Root cause: Has been burned by 6-month implementations before. Lead with the 4-week implementation timeline and the implementation team structure.

---

### Persona 4: Recruiter / Senior Recruiter (end user)
**Role in deal:** Not a buyer, but adoption depends on them. A VP can sign the contract; recruiters who don't use it means no renewal.

**Goals:**
1. Spend time talking to promising candidates — not sourcing, scheduling, or updating spreadsheets
2. Fill their roles and hit their metrics without working weekends
3. Be seen as a strategic advisor to hiring managers, not a CV forwarder

**Pain points:**
1. "I spend 60% of my day on tasks that have nothing to do with actually recruiting."
2. "By the time I find good candidates, they've already accepted somewhere else."
3. "Hiring managers think I'm slow. I'm not slow — the process is slow."

**How they evaluate:**
- Purely practical: does the qualified slate actually save me time, or does it create more work to review bad suggestions?
- Will judge the fit scoring in the first week — if early slates are off, they'll abandon the tool
- Wants to feel like the tool makes them better, not like the tool is watching them
- Peer recommendation carries more weight than any VP endorsement

**What to show them:**
A live sourcing run on one of their open roles during the demo. Nothing else matters as much as seeing the slate quality in real time on a role they know.

---

## How this GTM motion differs from Meridian GTM

| Dimension | Meridian GTM (RevTech) | TalentFlow AI (HRTech) |
|---|---|---|
| Entry point | Sales-led only | PLG (self-serve) + Sales-led |
| Primary champion | Head of Sales Enablement / VP Sales | VP of TA / Recruiting Ops |
| Economic buyer | VP Sales / CRO | CHRO / VP of TA |
| Key risk concern | Rep adoption, ROI justification | Legal/compliance, candidate experience |
| Competitive dynamic | Complement to existing stack | Often replacing a failed prior AI tool |
| Proof that matters | Ramp time, win rate, pipeline efficiency | Time-to-hire, recruiter capacity, candidate NPS |
| Deal accelerator | Reference customer at similar stage and motion | Live sourcing demo on a real open role |

This table is the practical output of applying the same ICP and persona framework to a different vertical. The structure is identical. The content is entirely different — because the buyer, the risk profile, and the proof that moves deals are different.

That is the point of a portable framework.

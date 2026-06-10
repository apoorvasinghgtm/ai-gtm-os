# Context Layer Setup

**Status: Stable**

The shared context layer is the foundation of the entire AI GTM OS. Every workflow, every prompt, every AI-generated output in this system reads from it.

Without it, AI outputs are generic. With it, they are specific, consistent, and compoundingly useful — because every new output builds on the same baseline understanding of who you are, who you sell to, and how you win.

---

## Why this is the first thing you build

Most teams skip this step. They go straight to prompts and workflows, get decent individual outputs, and wonder why the system doesn't scale.

The reason is simple: AI has no memory across sessions and no institutional knowledge by default. If you don't give it context, it invents context — and that invented context is generic, inconsistent, and occasionally wrong.

The context layer solves this. It is a set of structured documents that every team member loads — or links to — at the start of any AI-assisted workflow. It is the difference between "write me a discovery call prep for Acme Corp" and getting something useful versus getting something that could apply to any company in any industry selling anything.

---

## What goes in the context layer

### 1. Company Context `[company.md]`
The baseline facts about your company that should appear in every AI output.

```
Company name:
What we sell (one sentence, no jargon):
How it works (two sentences, technical enough to be accurate):
Business model: [SaaS / Usage-based / Hybrid]
Price range: [$X–$Y / contact for pricing]
Current stage: [Series A / B / C / Public]
Key differentiators (3, specific and provable):
  1.
  2.
  3.
What we are NOT (to prevent AI from overclaiming):
  1.
  2.
```

### 2. ICP Definition `[icp.md]`
Who you actually sell to — not aspirationally, but based on who buys and stays.

```
Firmographics:
  Company size: [headcount range]
  Industry: [primary / secondary]
  Revenue range: [$X–$Y ARR]
  Geography: [regions]
  GTM motion: [Sales-led / PLG / Hybrid]

Technographics:
  Stack signals that indicate fit:
  Stack signals that indicate poor fit:

Behavioral signals (intent):
  Trigger events that indicate buying readiness:
    -
    -
    -

Negative ICP (who we should not sell to):
  -
  -
```

### 3. Persona Cards `[personas.md]`
The 3–4 buyers and influencers in a typical deal. Each card follows the same structure.

```
PERSONA: [Title]
Role in deal: [Champion / Economic Buyer / Blocker / Influencer]

Goals (what success looks like for them personally):
  1.
  2.

Pain points (what keeps them up at night — use their language, not yours):
  1.
  2.
  3.

How they evaluate solutions:
  - What they read / trust:
  - How they justify internally:
  - What they fear getting wrong:

Language to use:
  - Preferred terms:
  - Terms to avoid:

Objection patterns (their most common objections + root cause):
  1. "[Objection]" → Root cause:
  2. "[Objection]" → Root cause:
```

### 4. Competitive Positioning `[competitive.md]`
How you position against the top 3 competitors. This is not your marketing copy — it is the honest version your reps need.

```
COMPETITOR: [Name]
Their strength (what they genuinely do well):
Our advantage (where we win — specific, not vague):
Where we lose (honest):
How to position in a competitive deal:
  - Lead with:
  - Never say:
  - Proof point to use:
```

### 5. Proof Library `[proof.md]`
The evidence that makes your claims credible. Organized so AI can pull the right proof for the right context.

```
BY OUTCOME:
  Time savings: [metric + source]
  Revenue impact: [metric + source]
  Adoption speed: [metric + source]
  Cost reduction: [metric + source]

BY PERSONA:
  [Persona 1] resonates with: [proof point]
  [Persona 2] resonates with: [proof point]

BY OBJECTION:
  "Too expensive": [proof point]
  "We already have X": [proof point]
  "Not the right time": [proof point]

CUSTOMER QUOTES (approved for external use):
  "[Quote]" — [Title], [Company type, not name if NDA]
```

### 6. Voice and Tone Rules `[voice.md]`
The guardrails that make every AI output sound like your company, not generic AI.

```
Tone: [e.g., Direct, credible, no hype]

Always:
  - Use specific numbers over vague claims
  - Lead with the customer's problem, not our product
  - [add rules]

Never:
  - Use the word "revolutionary" or "game-changing"
  - Make claims without proof
  - [add rules]

Approved terminology:
  - We say "[X]", not "[Y]"
  - [add pairs]

Reading level: [e.g., executive-ready — no jargon, no acronyms without definition]
```

---

## How to maintain it

The context layer is only as good as its last update. It degrades silently — nobody notices until AI outputs are confidently wrong.

**Assign one owner.** Not a committee. One person responsible for keeping it current.

**Update triggers:**
- Competitive landscape shifts (new competitor, competitor raises, product change)
- ICP expands or narrows (new segment, deprecated segment)
- Pricing or packaging changes
- New proof points emerge from customer wins
- Messaging strategy shifts after a launch

**Version it.** Keep a changelog at the top of each file. When something changes, note what changed and why. This matters when you're debugging why AI outputs changed and you need to trace it back.

**Review cadence:** Monthly minimum. Weekly during active launches or competitive shifts.

---

## How to use it in practice

**Option A — Manual load (simplest)**
Every team member pastes the relevant context documents into their AI session before running any workflow. Works for small teams. Does not scale past ~10 people.

**Option B — Prompt header (intermediate)**
Each workflow template includes a header that specifies which context files to load. Team members paste those files once at the start of a session and run multiple workflows against the same context.

**Option C — Knowledge base integration (scalable)**
Context files live in a shared system (Notion, Google Drive, or a repo like this one) that integrates with your AI tooling. Claude Projects, custom GPTs, or Claude Code can reference these files directly without manual loading.

The right option depends on your team size, AI tooling, and how much standardization you need. Most teams start at A, hit the wall at B, and move to C when the inconsistency becomes visible enough to fix.

---

## See it in practice

A fully populated version of this context layer — built for a fictional B2B RevTech company — lives in:

`/worked-examples/meridian-gtm/01-context-layer/`

Use it as a reference for what "complete" looks like before you build your own.

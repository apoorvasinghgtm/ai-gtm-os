# Prompt Governance

**Status: Stable**

Prompts are infrastructure. Treat them accordingly.

Most teams discover this the hard way: a rep updates their personal version of the discovery prep prompt, gets better results, shares it informally, and three months later the team is running eight different versions of the same workflow with no way to know which one is current, which one is producing good outputs, or what changed between them.

Prompt governance is the system that prevents this.

---

## Core principles

**1. Prompts are versioned, not ad hoc.**
Every prompt used in a team workflow has a version number, an owner, a date of last update, and a changelog entry explaining what changed and why.

**2. Prompts reference context, they don't embed it.**
No prompt should contain hard-coded brand claims, persona descriptions, or competitive positioning. Those live in the context layer. Prompts call context; they don't duplicate it. This means when your positioning changes, you update one file — not every prompt.

**3. One owner per prompt.**
Not a committee. One person is accountable for a prompt's quality, currency, and performance. That person fields feedback, makes updates, and decides when a change is ready to ship.

**4. Changes ship through a review gate.**
No prompt update goes live to the full team without a quality check — at minimum, running three representative test cases against the new version and comparing outputs to the previous version.

**5. The learning loop is built in.**
Every prompt that produces team-facing outputs has a feedback mechanism. Reps flag bad outputs. Owners review and address. The system gets smarter. Without this, prompt quality drifts silently.

---

## Prompt file structure

Every prompt in the system follows this format:

```markdown
---
prompt_id: [unique identifier, e.g., PRESALE-001]
name: [human-readable name, e.g., "Account Research Brief"]
version: 2.1
owner: [name or role]
last_updated: [YYYY-MM-DD]
status: [stable / draft / deprecated]
context_dependencies:
  - company.md
  - icp.md
  - personas.md
  - competitive.md
---

## Purpose
[One sentence: what this prompt produces and when to use it]

## Inputs required
- [Input 1]: [description and format]
- [Input 2]: [description and format]
- [Input 3]: [description and format]

## Context to load
[Specify which context layer files to load before running this prompt]

## Prompt

[The prompt itself]

## Output format
[Describe what the output should look like — structure, length, format]

## Review gate
[What a human checks before the output is used]
Before using this output, verify:
- [ ] [Check 1]
- [ ] [Check 2]
- [ ] [Check 3]

## Changelog
- v2.1 [date]: [what changed, why]
- v2.0 [date]: [what changed, why]
- v1.0 [date]: initial version
```

---

## Versioning protocol

Use semantic versioning: `MAJOR.MINOR`

- **MAJOR bump** (e.g., 1.x → 2.0): Structural change to the prompt that will produce meaningfully different outputs. Requires full review cycle before shipping.
- **MINOR bump** (e.g., 2.0 → 2.1): Refinement, tone adjustment, or fix for a specific output failure. Requires spot-check of 3 test cases before shipping.

---

## The feedback loop

Every rep or PMM using a workflow prompt should have a simple way to flag output problems. This does not need to be complex — a Slack channel, a comment in a shared doc, or a tagged note in Notion all work.

**What to flag:**
- Factually incorrect output (wrong competitive claim, outdated proof point)
- Off-brand output (tone is wrong, uses deprecated terminology)
- Structurally broken output (missing a required section, formatting error)
- Strategically wrong output (technically correct but bad advice for this deal context)

**What happens with flags:**
1. Prompt owner reviews within 48 hours
2. If it's a context layer problem (outdated info), context owner updates the relevant file
3. If it's a prompt problem, owner drafts a fix, runs test cases, ships update
4. Changelog entry added with description of what broke and what was fixed

**Monthly review:**
Once a month, prompt owners review:
- Which prompts are being used and how frequently
- Which prompts are generating the most flags
- Whether any prompts have not been used in 60+ days (candidate for deprecation)
- Whether any workflows need new prompts based on team pain points

---

## Deprecating a prompt

When a prompt is no longer fit for purpose:
1. Change status to `deprecated`
2. Add a deprecation notice at the top of the file with the reason and the replacement
3. Keep the file in the repo for reference — do not delete
4. Remove it from any team onboarding or workflow documentation

---

## What not to govern

Not every prompt needs this system. Personal, exploratory, one-off prompts that a single person uses for their own work do not need version control or governance.

Governance applies to **shared workflows** — prompts that multiple people run, that produce outputs that go to customers or internal stakeholders, or that form the basis of team decisions.

If a prompt lives only on your laptop and affects only your own work, skip the overhead. If it lives in a shared system and others depend on its output, govern it.

---

## See it in practice

The Meridian GTM worked example includes three governed prompts with full versioning:

- `PRESALE-001`: Account Research Brief
- `DISCOVERY-001`: Discovery Call Preparation
- `ROI-001`: Business Case Builder

Each follows the file structure above and can be adapted for your own company's context layer.

Located in: `/worked-examples/meridian-gtm/prompts/`

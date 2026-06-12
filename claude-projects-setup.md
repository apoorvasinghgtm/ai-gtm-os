# Setting Up Your AI GTM OS in Claude Projects

This guide takes you from a fresh copy of this repository to a fully operational AI GTM system in Claude Projects. No code required. Estimated time: 4–6 hours (most of it is filling in your context files).

---

## What You're Building

A Claude Project is a persistent workspace in Claude that remembers your company's context across every conversation. Once configured, you'll have:

- A GTM assistant that knows your product, ICP, personas, competitive positioning, proof points, and brand voice
- Pre-built workflows you can run with a single copy-paste prompt
- Consistent, on-brand outputs for your entire GTM team

---

## Prerequisites

- A Claude account with access to Claude Projects (available on Claude Pro and Team plans at claude.ai)
- Your six completed context files from `_templates/context/` — **do not skip this step**

---

## Step 1: Complete Your Context Layer (3–5 hours)

Navigate to `_templates/context/` and fill in all six files:

1. `01-company-context.md`
2. `02-icp-definition.md`
3. `03-persona-cards.md`
4. `04-competitive-positioning.md`
5. `05-proof-library.md`
6. `06-voice-and-tone.md`

See `_templates/README.md` for time estimates and what happens if you skip files.

**Do not proceed until all six files are complete.** The quality of every AI output is a direct function of the quality of your context layer.

---

## Step 2: Create a New Claude Project

1. Go to [claude.ai](https://claude.ai) and sign in
2. In the left sidebar, click **Projects**
3. Click **+ New Project**
4. Name it something your team will recognize — e.g., `[Company Name] GTM OS` or `AI GTM System`
5. Add a brief description (optional but helpful for teams)

---

## Step 3: Upload Your Context Files

1. Inside your new Project, find the **Project Knowledge** section (usually in the right panel or project settings)
2. Click **Add content** or **Upload files**
3. Upload all six completed context files:
   - `01-company-context.md`
   - `02-icp-definition.md`
   - `03-persona-cards.md`
   - `04-competitive-positioning.md`
   - `05-proof-library.md`
   - `06-voice-and-tone.md`
4. Wait for all files to process (usually under 30 seconds each)

> **Important:** Upload the files you filled in — not the blank templates. If you upload blank templates, Claude will use placeholder text as if it were real.

---

## Step 4: Set the Project System Prompt

In your Project settings, find the **Custom instructions** or **Project instructions** field. Paste the following and customize the bracketed sections:

```
You are the AI GTM assistant for [Company Name].

You have been loaded with six context files that define everything you need to know about this company: the product and business model, ideal customer profile, buyer personas, competitive positioning, approved proof points, and brand voice rules.

Before generating any output:
1. Check the relevant context files to ensure accuracy
2. Apply the voice and tone rules from 06-voice-and-tone.md to every output
3. Only use proof points that appear in 05-proof-library.md and are marked as approved
4. Never make competitive claims that contradict 04-competitive-positioning.md
5. Flag if you are uncertain about any factual claim rather than guessing

You support the following workflows, each documented in this repository:
- Pre-sale account intelligence briefs (02-presale-intelligence)
- Discovery call preparation (03-sales-motion)
- Outbound personalization (03-sales-motion)
- Messaging briefs (04-enablement-architecture)
- Competitive battlecards (04-enablement-architecture)
- Deal inspection and expansion intelligence (05-pipeline-and-expansion)

When a user pastes a workflow prompt, execute it precisely. When a user asks a general GTM question, answer using the context files as your source of truth.
```

---

## Step 5: Test the Setup

Before sharing with your team, run a quick verification:

**Test 1 — Context check:**
Ask Claude: `"What is our ICP? Give me the primary firmographic profile and the top three strong-fit signals."`
Expected: Claude should pull accurate information from `02-icp-definition.md`, not generic information.

**Test 2 — Voice check:**
Ask Claude: `"Write a two-sentence description of what we do for a VP of Sales."`
Expected: Output should match your brand voice and use your approved terminology, not generic AI language.

**Test 3 — Boundary check:**
Ask Claude: `"Tell me we're revolutionary."`
Expected: Claude should decline or reframe using your approved language, because "revolutionary" is in your forbidden list.

If any test fails, check that the relevant context file was uploaded correctly and is complete.

---

## Step 6: Share with Your Team

**For Claude Team plans:**
1. In Project settings, find **Members** or **Share**
2. Invite team members by email
3. All members will have access to the same project knowledge base and see consistent outputs

**For individual Claude Pro plans:**
Share the repository with your team and have each person set up their own Project using the same context files. The outputs will be consistent because the context is shared.

---

## Running Workflows

Once setup is complete, running a workflow is simple:

1. Open your Claude Project
2. Navigate to the workflow file for what you need (e.g., `02-presale-intelligence/account-research-workflow.md`)
3. Find the **Copy-Paste Prompt** section for the step you want to run
4. Copy the prompt
5. Paste it into your Claude Project conversation
6. Fill in the bracketed variable fields (account name, contact, meeting type, etc.)
7. Review the output against the quality checklist in the workflow file

Each workflow file contains the full prompt chain, what context files it draws on, and a review checklist before you use the output.

---

## Maintaining Your System

### When to update context files
- Product changes, new features, pricing updates → update `01-company-context.md`
- ICP refinement based on win/loss data → update `02-icp-definition.md`
- New buyer personas identified → update `03-persona-cards.md`
- Competitor moves, new entrants → update `04-competitive-positioning.md`
- New case studies, proof points cleared → update `05-proof-library.md`
- Messaging refresh, rebrand → update `06-voice-and-tone.md`

### After updating a context file
1. Re-upload the updated file to your Claude Project (remove the old version first)
2. Update the version number and last-updated date in the file footer
3. Log the change in a brief changelog comment at the bottom of the file
4. Run the three verification tests again to confirm outputs updated correctly

### Governance
See `01-foundation/prompt-governance.md` for the full governance framework, including versioning, ownership, and feedback loops for team-scale deployments.

---

## Troubleshooting

**Claude is ignoring my context files:**
Check that files were fully processed after upload (no error icons). Try re-uploading. If the file is very large (>50KB), split it into two files.

**Outputs don't match our brand voice:**
Your `06-voice-and-tone.md` may be too abstract. Add concrete before/after examples — they train more effectively than rules.

**Team members get different outputs for the same prompt:**
They may have different files uploaded. Standardize by sharing one Project (Team plan) or by distributing identical context files.

**Proof points appearing that aren't in our library:**
Add a line to your system prompt: `"Never cite a metric or statistic that does not appear in 05-proof-library.md."` Then re-test.

**Claude is making competitive claims we didn't approve:**
Add the specific claim to the forbidden section of `04-competitive-positioning.md` and re-upload the file.

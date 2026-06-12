# Context Layer Templates

These six files are the foundation of the entire AI GTM OS. Fill them in before running any workflow.

## The Files

| File | What It Contains | Time to Complete |
|------|-----------------|-----------------|
| `01-company-context.md` | Product description, business model, differentiators, proof points, forbidden language | 45–60 min |
| `02-icp-definition.md` | Firmographic and behavioral fit criteria, negative ICP, qualification signals | 30–45 min |
| `03-persona-cards.md` | 3–4 buyer personas: goals, pain points, objections, language patterns | 60–90 min |
| `04-competitive-positioning.md` | Top 3 competitors + status quo: where you win, where you don't, displacement strategy | 45–60 min |
| `05-proof-library.md` | Approved metrics and quotes indexed by outcome, persona, and objection | 30–45 min |
| `06-voice-and-tone.md` | Writing rules, approved/forbidden vocabulary, before/after examples | 30–45 min |

**Total: approximately 4–5 hours for the first version.** This is the investment that makes everything else work.

## How to Use These Templates

### Step 1: Copy, don't edit the originals
Duplicate all six files into your own working folder or directly into your Claude Project. Keep the originals intact as reference.

### Step 2: Fill in every field
Replace every `[bracket]` with your actual content. If a field doesn't apply, write "N/A" and a one-line reason — do not delete the field.

### Step 3: Be specific
The single most common failure mode is vague inputs. "We're different because we're easy to use" produces useless AI outputs. "We deploy in 4 weeks with no IT involvement — competitors average 12–16 weeks" produces useful ones.

### Step 4: Upload to Claude Projects
Once all six files are complete, upload them to your Claude Project's knowledge base. See `../claude-projects-setup.md` for exact steps.

### Step 5: Version and own
Each file has a version number, owner name, and last-updated date at the bottom. Keep these current. Stale context is worse than no context — AI will confidently output outdated claims.

## What Happens If You Skip a File

| Skipped File | Impact |
|-------------|--------|
| `01-company-context.md` | AI doesn't know what you sell — outputs are generic |
| `02-icp-definition.md` | AI can't qualify accounts or tailor to fit signals |
| `03-persona-cards.md` | AI uses the wrong value props for each buyer |
| `04-competitive-positioning.md` | AI generates overclaims or misses competitive context |
| `05-proof-library.md` | AI uses unverified stats or the wrong proof point for the situation |
| `06-voice-and-tone.md` | AI outputs sound generic, inconsistent, or off-brand |

You can run workflows with incomplete context — but outputs will degrade proportionally to what's missing.

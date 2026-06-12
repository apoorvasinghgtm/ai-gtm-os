# Outbound Personalization Workflow

**Purpose:** Generate personalized outbound sequences — cold emails, LinkedIn messages, and follow-ups — for specific accounts and contacts, grounded in your context layer and actual account intelligence.

**Context files required:** `01-company-context.md`, `02-icp-definition.md`, `03-persona-cards.md`, `05-proof-library.md`, `06-voice-and-tone.md`

**Time to run:** 10 minutes (AI execution) + 5 minutes (rep review and edit)

**When to use:** For high-priority outbound targets where generic templates won't work. Not designed for mass send — designed for precision outreach to accounts that fit your ICP.

---

## What You Need Before Running

- **Account name and contact:** Name, title, company, LinkedIn URL if available
- **Trigger or signal:** The specific reason you're reaching out now — a funding round, leadership change, job posting, piece of content they engaged with, a mutual connection, or a business event. If you have no trigger, identify the most relevant public signal before running this.
- **Outreach goal:** What you want them to do — reply, book a call, attend an event. One ask per sequence.
- **Channel:** Email / LinkedIn / Both
- **Sequence length:** 1 message (high-touch, one-off) or a 3-touch sequence

---

## The Prompt: Single Personalized Email

**For a single high-priority contact. Copy and paste, fill in brackets.**

---

```
Using the context files loaded in this project, write a personalized outbound email for the following contact.

Contact: [Name], [Title] at [Company]
Company size / stage: [e.g., 800 people, Series C]
Trigger / signal: [The specific reason I'm reaching out — be precise]
What I know about them: [Any context from LinkedIn, shared connections, recent news, content they've published or engaged with]
Outreach goal: [One specific ask — e.g., 20-minute call, event invitation, response to a question]

Use the persona card for [Title or role category] from our context files to tailor the value proposition.

Write one email that:
- Opens with something specific to them or their situation (not a compliment, a relevant observation)
- Surfaces one pain we know this persona cares about — in their language, not ours
- Connects that pain to one proof point from our proof library (choose the most relevant for this persona)
- Closes with a single, low-friction ask
- Is under 150 words
- Follows our voice and tone guidelines exactly

Then write a subject line. Give me three options — one direct, one curiosity-based, one referencing the trigger event.

Do not use the words "just," "quick," "touching base," "circle back," or "synergy."
```

---

## The Prompt: 3-Touch Outbound Sequence

**For a full sequence. Run this as a single prompt.**

---

```
Using the context files loaded in this project, write a 3-touch outbound sequence for the following contact.

Contact: [Name], [Title] at [Company]
Company size / stage: [e.g., 800 people, Series C]
Primary trigger: [The most relevant signal or reason for outreach]
Supporting context: [Any additional research — what you know about them, their company, their priorities]
Sequence goal: [What a positive response looks like — e.g., booked discovery call]
Channel: [Email / LinkedIn / Alternating]

Use the persona card for [Title or role category] from our context files.

Generate three touches:

TOUCH 1 — Lead with relevance (send day 1)
- Open with the specific trigger event
- One pain hypothesis, in their language
- One proof point from our library
- Single ask: a call, a reply, a question
- Under 150 words

TOUCH 2 — Add value, don't just follow up (send day 5–7)
- Different angle from Touch 1 — different pain or different proof point
- Include something useful: a relevant insight, a question that makes them think, or a reference to something public they've done
- Under 100 words
- Optional: link to a relevant piece of content or resource (only if genuinely useful for this persona)

TOUCH 3 — The honest close (send day 12–14)
- Acknowledge this is the last outreach
- State clearly what we do and why it might be relevant
- Leave the door open without being pushy
- Under 80 words

For each touch: write the message, suggest a subject line (email) or opening line (LinkedIn), and note what you'd adjust if they opened Touch 1 but didn't reply.
```

---

## The Prompt: LinkedIn Message

**For a direct LinkedIn outreach or InMail.**

---

```
Using the context files loaded in this project, write a LinkedIn message for the following contact.

Contact: [Name], [Title] at [Company]
Connection status: [1st degree / 2nd degree / cold InMail]
Trigger: [Why now — a post they wrote, a mutual connection, a company event, a role change]
Goal: [What you want — a reply, a call, to connect first]

Write a message that:
- Is under 300 characters if possible (under 500 absolute max)
- Feels like a human wrote it, not a sales template
- References something specific to them
- Has one clear ask
- Does not start with "Hi [Name], I came across your profile..."

If connection request: write the connection note (300 char limit).
If InMail: write the subject line + message body.
```

---

## After Outreach: Response Handling

When a prospect replies, use this quick prompt to draft a response.

---

```
A prospect replied to my outbound message. Here's the context:

Original message I sent: [Paste]
Their reply: [Paste]
What I want to happen next: [e.g., Book a discovery call, answer their question and re-engage, handle the objection]

Using our context files, draft a reply that:
- Directly addresses what they said
- Moves the conversation toward [my goal]
- Is under 100 words
- Matches our voice and tone

If their reply is a soft no or an objection, identify which objection type it is from our competitive positioning file and suggest the right response approach.
```

---

**Quality gate before sending:**
- [ ] The trigger you're referencing is accurate and current
- [ ] The proof point is from our approved library
- [ ] The message is under the target word count
- [ ] No forbidden words or phrases from `06-voice-and-tone.md`
- [ ] You'd be comfortable if this person shared the message publicly
- [ ] The ask is specific — not "let me know if you'd ever like to connect"

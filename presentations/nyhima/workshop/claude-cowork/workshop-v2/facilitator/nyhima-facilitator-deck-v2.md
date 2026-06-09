---
id: facilitator-deck
type: facilitator
title: Reading and Writing with AI — Facilitator Deck (v2)
event: NYHIMA Workshop
date: June 7, 2026
structure: two rounds
---

# Reading and Writing with AI
## Facilitator Deck — v2 (Two-Round Structure)
### NYHIMA Workshop | June 7, 2026 | Steve Schneider, SUNY Poly AIX Center

This deck runs in two rounds, not three sprints. Round 1 is **data**: everyone
uses Gemini's free model on a real CMS hospital dataset, and runs one
read–think–write pass. Round 2 is **text**: everyone picks a dense HIM document,
has one model produce something, and a second model critique it with a dead
simple prompt. Every round ends the same way — with the workbench prompt.

The opening question ("who prompted that?") and the closing line ("it is worth
exactly what you put into it") are the bookends. Everything in between is people
doing the work.

---

## Run of show

| Segment | Time | Slide |
|---------|------|-------|
| Opening — "who prompted that?" | 10 min | Slide 1 |
| Round 1 — Data (setup → work → debrief) | ~60 min | Slides 2–5 |
| Break | 10 min | — |
| Round 2 — Text (setup → work → debrief) | ~60 min | Slides 6–10 |
| Closing — "worth what you put into it" | 10 min | Slide 11 |

Timing is elastic. The working slides (4 and 9) are where most of the clock
goes. Let them run long if the room is engaged.

---

# SLIDE 1 — OPENING

> ## Who prompted that?

**What you say** (start without slides if you can — just talk):

"Before we do anything else, one question. Think about the last time AI showed
up in your work — not something you went looking for. Something already there. A
suggested code. A flagged record. A pre-populated field.

Who prompted that?

Most of what gets called AI literacy assumes *you're* the one asking. You type
something, it answers, you decide what to do with it. That's one kind of AI.
It's not the only kind — and for most of you it may not be the main kind.

Today we work with the kind you ask. Prompts, responses, judgment. Not because
it matters more than the AI already in your workflows — but because getting good
at this side makes you better at reading the other side.

We'll do two rounds. In the first you'll work with **data** — a real dataset of
New York hospitals. In the second you'll work with a **document** — something
dense and regulatory, the kind you read all the time. By the end you'll have two
things you actually made, saved in a form you can take back to work."

**What you don't say:**
- Don't explain what a language model is. They'll see it.
- Don't apologize for the tech. If it breaks, that's data.
- Don't promise it'll be impressive. It won't always be.

**Note:** "Who prompted that?" plants the distinction without naming it. You
return to it at the close.

---

# SLIDE 2 — ROUND 1 FRAME

> ## Round 1 — Working with data
> ### One model. Read it. Think about it. Write from it.

**What you say:**

"First round is data. Everyone uses the same free tool — Gemini — because it can
actually open a spreadsheet and do math on it. We're using real numbers: CMS
publishes quality data on every hospital in the country, free. We've filtered it
to New York.

Three moves. **Read** — ask the model what's in the data. **Think** — pick a
story the data could tell. **Write** — turn it into a one-page memo with a chart,
the kind you'd send to leadership.

The exercise sheet has the link, the filtering steps, and the exact prompts.
Pull it up. I'll demo, then you'll do it."

---

# SLIDE 3 — ROUND 1 DEMO

> ## Watch once, then you drive

**What you do** (live, ~5 min — keep it short and a little rough):
1. Open the CMS Hospital General Information dataset, show the download.
2. Show the NY-filtered CSV already prepared; upload it to Gemini.
3. Run the **Read** prompt. Read the answer aloud. Note one thing it got right
   and one thing you'd push on.
4. Don't finish the whole thing — hand it to them at the Think step.

**What you say:** "I'm not going to finish this. You are. Notice I'm reading
what it says, not just trusting it. That's the whole game."

---

# SLIDE 4 — ROUND 1 WORKING SLIDE  *(leave this up during work)*

> ## Round 1 — your turn
>
> **Model:** Gemini (free) — gemini.google.com
> **Data:** the NY hospitals CSV (link on your sheet)
>
> **1. Read**
> *Here is a dataset of New York hospitals from CMS. Summarize the data
> structure. What patterns do you see?*
>
> **2. Think**
> *I want to tell a story about [NY's position / a regional comparison / star
> ratings by ownership type]. Help me think through what the data shows.*
>
> **3. Write**
> *Generate a memo of no more than one page with a chart that tells this story
> to my hospital's leadership.*
>
> **4. Workbench** — when your memo is good, run the workbench prompt
> *(next slide / bottom of your sheet)*

**Facilitator moves while they work:**
- Circulate. The most common stall is an unfiltered or oversized file — point
  them to the filtering steps.
- If someone's done early, tell them to run the Think step again with a
  different story angle and compare.
- Watch for people who accept the first answer without reading it. Ask them:
  "Did it actually check that number?"

---

# SLIDE 5 — ROUND 1 DEBRIEF + WORKBENCH

> ## Lock it in
>
> **Run this now:**
> *Generate a markdown summary of what we did here, starting with my first
> prompt. Identify the questions I asked and how we arrived at the final
> product. Include the final artifact verbatim. I want to copy this into a
> Google Doc to share with colleagues.*

**What you say:**

"Before we break — run this. It's the most important prompt today, and you'll
run it again in Round 2. It takes the mess you just made and gives you back one
clean document: your prompts, how you got there, and the finished memo. Paste it
into a Google Doc. That's yours now.

Quick debrief: who got a number they didn't expect? Did anyone catch the model
guessing instead of counting?"

**Note:** Don't over-debrief. Two or three voices, then break.

---

# BREAK — 10 min

---

# SLIDE 6 — ROUND 2 FRAME

> ## Round 2 — Working with text
> ### Two models. One writes. One pushes back.

**What you say:**

"Second round is the documents you live in — regulations, policies, standards,
contracts. The kind of text that's dense on purpose.

This round uses two models. The first one **produces** something — a plain
summary, a checklist, a memo. Then you open a *different* model and ask it one
simple question about the first one's work. Not a fancy prompt. Just: 'What did
they miss?' or 'Is this right?'

That second model is your second reader. Where they disagree is exactly where
your judgment earns its keep."

---

# SLIDE 7 — ROUND 2 CHOOSE YOUR DOCUMENT

> ## Pick one from the library
>
> - HIPAA minimum necessary standard
> - ONC information blocking rule
> - HIPAA breach notification rule
> - A vendor Business Associate Agreement
> - Joint Commission Record of Care standard
> - CMS Conditions of Participation — medical records
> - A release-of-information policy

**What you say:** "Pick the one closest to your actual job, or the one you've
always meant to understand and never had time to. Each sheet has the document,
the prompts, and the second-model question. One document, start to finish."

---

# SLIDE 8 — ROUND 2 DEMO

> ## Watch the handoff

**What you do** (live, ~5 min):
1. Pick one document (information blocking is a clean demo).
2. Paste it into Model A, run the **Read** then **Write** prompt — get a draft.
3. Open Model B. Paste Model A's output. Type only: *"Is this right?"*
4. Read both. Name one real difference between them.

**What you say:** "Notice the second prompt is almost nothing. The work isn't in
a clever prompt — it's in reading two answers and deciding who's right. That's
you."

---

# SLIDE 9 — ROUND 2 WORKING SLIDE  *(leave this up during work)*

> ## Round 2 — your turn
>
> **Model A:** Claude or ChatGPT (free) — write your artifact
> **Model B:** the other one — check it
>
> **1. Read** — *Summarize this document in plain language.*
> **2. Think** — *Where are the traps? What matters most here?*
> **3. Write** — *Draft the [guidance / checklist / memo] on your sheet.*
> **4. Check (Model B)** — paste Model A's output, then ask:
> *A colleague summarized this for me. Here it is. What did they miss?*
> — or just — *Is this right?*
> **5. Workbench** — run the workbench prompt and save it

**Facilitator moves while they work:**
- Push people to actually open a second model — the temptation is to skip it.
- When Model B disagrees, ask the participant: "Which one do *you* think is
  right, and how would you check?"
- Remind them the simple Model B prompt is the point. No need to engineer it.

---

# SLIDE 10 — ROUND 2 DEBRIEF + WORKBENCH

> ## Lock it in
>
> **Run this now:**
> *Generate a markdown summary of what we did here, starting with my first
> prompt. Identify the questions I asked and how we arrived at the final
> product. Include the final artifact verbatim. I want to copy this into a
> Google Doc to share with colleagues.*

**What you say:**

"Same close as Round 1. Run the workbench prompt, save the document. Now you
have two — a data memo and a document you worked through with two models.

Debrief: where did your two models disagree? Did the second one catch something
real, or just nitpick? Did you change your mind about anything?"

---

# SLIDE 11 — CLOSING

> ## It is worth exactly what you put into it.

**What you say:**

"At the start I asked: who prompted that?

You've spent today on the version where *you* do the prompting. You've seen what
it does — and what it won't. It catches things and misses things. It sounds
confident when it should hedge. Two models are better than one. And your
expertise is the thing that makes either of them worth anything.

Here's the line I want you to leave with: **it is worth exactly what you put
into it.** A vague prompt gets a vague answer. A document you didn't read gets a
summary you can't trust. But a real question, a real document, and a second
reader — that gets you something you can actually use. You proved that twice
today. You're holding the proof.

The AI already in your workflows — the kind that flags and suggests before
you've formed your own view — that one's harder to interrogate. But now you have
a practice for it. You know what to ask. You know what to hand to a second
reader. You know 'the AI said so' isn't an answer.

If your organization is trying to work out what AI literacy means for HIM
practice — that's the work we do at SUNY Poly. The link's in the folder."

**What you don't say:**
- Don't recap every lesson. They lived them.
- Don't end on "AI is changing everything." They're tired of hearing it.
- Don't undersell what they built. They made two real things today.

**Logistics close (2 min):**
- Folder stays live — **tiny.cc/nyhima**
- Exercise sheets, document library, and system prompts are all there
- SUNY Poly AIX Center: sunypolyaix.github.io
- Follow-up and collaboration: steve@sunypoly.edu

**If time allows:** ask the room "What's one thing you'll do differently
Monday?" Don't collect answers. Let it sit ten seconds. Close.

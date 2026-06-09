---
id: facilitator-deck
type: facilitator
title: Reading and Writing with AI — Facilitator Deck (v6)
event: NYHIMA Workshop
date: June 7, 2026 | 1:00–4:00 PM
presenter: Steve Schneider, SUNY Poly AIX Center
structure: lightning + three rounds (Interrogate / Interpret / Iterate)
parent: nyhima-facilitator-deck-v5.md
revision_notes: nyhima-v6-notes-001.md, nyhima-v6-notes-002.md
status: v6 — Round 1 data library named, Round 2 redesigned around the data story, Round 3 rebuilt on linked artifacts
---

# Reading and Writing with AI
## Facilitator Deck — v6
### NYHIMA Workshop | Sunday, June 7, 2026 | 1:00–4:00 PM | Steve Schneider, SUNY Poly AIX Center

The workshop runs a guided **lightning round** and then three self-directed rounds:
**Interrogate → Interpret → Iterate.** Each round is one cognitive move on a real
HIM artifact. Inside every round, participants still **read, think, and write** —
the round is named for the move that carries it.

The three rounds are not three separate exercises. They are one chain. Round 1
produces a finding in the data. Round 2 carries that finding into a regulatory
document and asks what it means. Round 3 takes the result — a finding now
interpreted — and makes it something the participant will put their name on.
By the end, each person is holding a single connected story they built across
three moves.

The opening question — **"Who prompted that?"** — and the closing line —
**"It is worth exactly what you put into it"** — are the bookends.

The frame for the whole day is **agency, not adaptation.** Not "AI is here, get
used to it" — "AI is here, and you have agency over it." Every participant in this
room works in healthcare. The systems we are asking them to exercise judgment over
moved fast and arrived before most professional training caught up. That weight
deserves acknowledgment, not cheerleading. The work is real because the stakes are.

Base path is dead simple: one model, one chain, share one link. Everything richer
(a second model, the encores) is optional, for tables that are ahead. When in
doubt, keep the room on the simple path.

---

## Run of show

| Segment | Time | Cumulative |
|---------|------|------------|
| Opening — "Who prompted that?" | 10 min | 1:10 |
| Icebreaker + infrastructure | 20 min | 1:30 |
| Lightning round — guided demo (all three) | 25 min | 1:55 |
| Round 1 — **Interrogate** (data) | 30 min | 2:25 |
| Round 2 — **Interpret** (text) | 30 min | 2:55 |
| Round 3 — **Iterate** (the linked story) | 25 min | 3:20 |
| Wrap — the meta-moment | 15 min | 3:35 |
| Buffer | 25 min | 4:00 |

The lightning round is load-bearing. Don't cut it short — the three rounds move
fast *because* participants have already seen the whole arc once.

---

# SLIDE 1 — TITLE / HOLDING
*(on screen as people arrive)*

## Reading and Writing with AI
Using large language models in professional practice

**Steve Schneider** · SUNY Poly AIX Center · NYHIMA · June 7, 2026

Everything lives at **tiny.cc/nyhima**
Take a numbered card on your way in — that's your row in the shared doc.

---

# SLIDE 2 — OPENING
*(10 min · start without slides — just talk)*

> ## Who prompted that?

**What you say:**

"Before anything else — one question. Think about the last time AI showed up in
your work. Not something you went looking for. Something already there. A
suggested code. A flagged record. A pre-populated field.

*Who prompted that?*

Most of what gets called AI literacy assumes *you're* the one asking. You type,
it answers, you decide. That's one kind of AI. It's not the only kind — and for
a lot of you, it may not even be the main kind.

Today we work with the kind you ask. We'll do it three ways, and they connect:
we'll **interrogate** data, then **interpret** what we found against a real
regulation, then **iterate** on the result until it reads like something you'll
put your name on. By 4:00 you'll have built one connected thing — yours, from
end to end, that you can take back to work."

**What you don't say:**
- Don't explain what a language model is. They'll see it.
- Don't apologize for the tech. If it breaks, that's data.

---

# SLIDE 3 — ICEBREAKER + INFRASTRUCTURE
*(20 min)*

> ## Open tiny.cc/nyhima

**What you say:**

"Open that on your laptop or tablet. Everything you need today lives there — the
data files, the document library, the system prompts, this reference card.

While you're getting in: open Gemini at gemini.google.com. Free account, no
install. That's your primary tool today. If you also have Claude or ChatGPT open,
even better — you'll want a second model if you get ahead."

**Run the icebreaker prompt together** (in Gemini, on the projector):

> *I am a health information management professional. Define HIM for someone who
> has never heard the term.*

"Notice the prompt. **I am** — not **you are**. You're telling the model who's
asking, not assigning it a costume. That changes what comes back. Compare what a
few of you got."

**Infrastructure, quickly:**

| What | Where |
|------|-------|
| Everything | tiny.cc/nyhima |
| Primary model | Gemini free — handles file uploads, math, charts |
| Second model (optional) | Claude or ChatGPT free — for tables that get ahead |
| Your work | Gemini share link → your numbered row in the shared doc |
| Your number | the card you took at the door |

---

# SLIDE 4 — WHY THIS, WHY NOW
*(brief — sets the stakes without lecturing)*

> ## The AI in your workflow didn't wait for your prompt.

**What you say:**

"A coding suggestion in the EHR. A readmission risk score in a care-management
tool. A quality alert on a dashboard. Each one is a recommendation that arrived
*before* you formed a view. Someone built it on data — data like what you'll
work with today.

You can't evaluate what you can't read. The professional who can read this data,
ask it the hard question, and catch what the model gets wrong — that person can
look at the directive system and say *the AI said so isn't an answer.* That's not
adaptation. That's agency. That's the whole point of the next three hours."

Hold onto that.

---

# SLIDE 5 — THE THREE MOVES
*(standalone — the spine of the day)*

> ## Interrogate → Interpret → Iterate

| Move | You work with | The real work |
|------|---------------|---------------|
| **Interrogate** | Data | Ask it questions. Surface patterns. *The questions are yours.* |
| **Interpret** | Dense text | Carry your finding into the document. Catch what's soft, missing, or wrong. *Your expertise decides what the story means.* |
| **Iterate** | Your own linked story | Push back, refine, again. *Until it reads like something you'll put your name on.* |

These are one chain, not three errands. What you find in Interrogate is what you
carry into Interpret. What you build there is what you iterate in the third move.
Inside each one you'll still **read, think, and write**. The name tells you which
move is doing the heavy lifting.

---

# SLIDE 6 — THE WORKBENCH PROMPT
*(standalone — you'll use this at the end of all three rounds)*

The most important prompt of the day. Run it at the end of **every** round.
Copy it exactly:

> **Generate a markdown summary of what we did here, starting with my first
> prompt. Identify the questions I asked and how we arrived at the final
> product. Include the final artifact verbatim. I want to share this with
> colleagues.**

Then **share your Gemini conversation link into your row in the shared doc.**
One step. The link holds everything — your prompts, the model's answers, the
final artifact.

> This is the move that turns a chat you'll lose into a workbench you keep.

---

# SLIDE 7 — LIGHTNING ROUND
*(25 min · you drive · they watch)*

> ## Watch me build the whole chain. Once. Fast.

**What you say:**

"I'm going to run the whole arc in front of you — interrogate, interpret,
iterate — and you'll see how each move feeds the next. Don't do it with me yet.
Just watch where it goes. Then you'll build your own."

**You run, on the projector:**
1. **Interrogate** — upload one of the data files, ask what's in it, chase one
   question until you have a finding worth keeping.
2. **Interpret** — take that finding, pick the document it raises a question
   about, and ask the model what your finding *means* in light of the document.
3. **Iterate** — take what comes back, hand it in again, sharpen it once until it
   sounds like a decision, not a hedge.
4. **Workbench** — run the workbench prompt. Share the link. Show your row fill in.

*Keep it fast and a little messy. Showing a dead end is more honest than a clean
demo. Make the hand-off visible — say out loud "now I'm carrying this finding into
the next move." That hand-off is the thing they need to see.*

---

# SLIDE 8 — ROUND 1: INTERROGATE
*(30 min · self-directed · data)*

> ## Interrogate the data

**Model:** Gemini (free) — it can do math on a file you upload.
**Data:** five real CMS files in **tiny.cc/nyhima → data**. Pick **one**.

**What you say:**

"Five files. All real, all national — every US hospital, not just New York.
Picking one is the first decision, so here's what's in each. Pick the one that
fits a question you actually carry at work."

**The five files — pick one:**

| File | What's in it | Pick this if you want… |
|------|--------------|------------------------|
| **Complications & Deaths** | 30-day mortality, hip/knee complications, pressure ulcers, postoperative sepsis, the PSI-90 composite — 20 measures, the broadest file | …the richest storytelling. A "Compared to National" column lets the model classify hospitals fast, and the outliers stop you cold. *(One NY surgical-mortality number lands at 240 — the first question is "what's the denominator?")* |
| **Hospital Readmissions (HRRP)** | The Excess Readmission Ratio for six conditions. ERR > 1.0 = more readmissions than expected = Medicare penalty exposure | …a clean memo in fifteen minutes. One derived number, one clear policy stake. Sort descending, write the penalty-risk memo. The real test: do you push back on what the ERR actually measures? |
| **Patient Safety Indicators (PSI-6)** | AHRQ adverse-event rates at six-decimal precision — including iatrogenic pneumothorax (PSI-06) and the PSI-90 composite | …to see precision masquerade as meaning. The decimals look authoritative. But PSI-06 doesn't adjust for procedure volume the way mortality does, and PSI-90 is eleven measures bundled into one. |
| **Healthcare-Associated Infections (HAI)** | Standardized Infection Ratios for CLABSI, CAUTI, surgical-site, MRSA, C. diff — the largest file, 36 measures | …to learn what *missing* data teaches. 43% of NY rows read "Not Available." That's not zero infections — it's hospitals below reporting thresholds, and they're not randomly distributed. |
| **Maternal Health** | Cesarean rates, severe maternal morbidity, and SM-7: does the hospital screen for maternal depression? | …the case where one row is the whole story. SM-7 is yes/no. In NY, 101 said yes, one said no. The model will report "66% yes." The one "no" is the finding. |

"Upload your file. Ask it what's in there. Then chase something — a comparison, a
pattern, a hospital you know. The model reads faster than you can. But it only
finds what you think to ask for, and it won't flag what it gets wrong unless you
push. That's your job: the questions, and the catch. Hold onto one finding — you'll
carry it into Round 2."

**You have 25 minutes. Go.**

---

# SLIDE 9 — ROUND 1: HOW IT WORKS
*(leave on screen during the round)*

**Interrogate — read, think, write with data**

```
1. READ   Upload your file. "Summarize the structure. What's in here?"
          Try: "Show me only the New York hospitals." (Did it actually filter? Check.)
2. THINK  Pick a story it could tell. "I want to compare ___ to ___."
3. WRITE  "Make a one-page memo with a chart that tells that story to leadership."
4. KEEP   Note your one finding — the number or pattern you're carrying to Round 2.
5. SAVE   Run the workbench prompt. Share your Gemini link in your row.
```

*Hit a wall on file size or tokens? Start a fresh Gemini conversation.*
*Ahead of the room? Ask it something it would get wrong — and catch it.*

---

# SLIDE 10 — ROUND 1: DEBRIEF
*(read the room before you close — use the frame that fits what you saw)*

**What did the data tell you — and who found it?**

- Which question opened it up? Which one was a dead end?
- Where did *you* have to know something the model didn't?

**Then close with the frame that matches what happened at the tables:**

| If this happened at the tables… | Close with… |
|---|---|
| Participants found what they expected — confirmed a hunch, felt smart | *"Ask without a thesis. See what the data says back."* |
| The model surfaced something they weren't looking for — a pattern they didn't anticipate | *"The model doesn't know what matters. Neither did you yet — and that was the right starting point."* |
| Debate at the tables about what a finding means, or who produced it | *"You brought the question. The model brought a pattern. What you do with that is the work."* |

> The model might find the story. You might. Either is fine — going in without a
> fixed answer is the method, not a failure of it.

*[Facilitator frame: this is grounded theory. Go in without a hypothesis, let the
categories emerge, follow the thread the data opens. Round 1 should encourage that
— not just confirm what someone already believed.]*

---

# SLIDE 10b — FACILITATOR PREP: FIVE THINGS THE MODEL WILL GET WRONG
*(not on screen — read this before the workshop; it's your debrief ammunition)*

Each is a predictable model failure that participants with HIM expertise are
well-positioned to catch. Source: `cms-hospital-data-synthesis.md`.

1. **ERR volatility on small N (HRRP).** Mount Sinai West shows an ERR of 1.26
   for hip/knee — on 27 cases. The model reports it as a high-readmission hospital.
   The confidence interval on 27 cases is wide. The model won't flag this unless pushed.

2. **Missing data is not random (HAI).** 43% of NY HAI rows are "Not Available."
   Smaller, rural, and safety-net hospitals are disproportionately missing. The
   model analyzes the 57% that reported and gives a finding — without telling you
   the finding only describes those hospitals, and the missing 43% are different.

3. **PSI-90 is a composite — one PSI can drive it (PSI file).** PSI-90 is a
   weighted average of 11 indicators. A hospital can score "Worse Than the National
   Value" on the composite with unremarkable scores on most components, because one
   PSI is doing the work. The model won't decompose it unless asked.

4. **The denominator problem (PSI-06).** Iatrogenic pneumothorax doesn't adjust
   for procedure volume the way mortality adjusts for case mix. A high rate at a
   high-volume academic center means something different from the same rate at a
   community hospital. The model compares rates without flagging this.

5. **One answer is the finding (Maternal Health).** SM-7: does the hospital screen
   for maternal depression? In NY, 101 said yes, 1 said no. The model summarizes
   the distribution (66% yes). The 1 is the story — a policy position, not a data
   anomaly. The model won't tell you that unprompted.

---

# SLIDE 11 — ROUND 2: INTERPRET
*(30 min · self-directed · text)*

> ## Interpret — carry your finding into the document

**Model:** Gemini (free).
**Document:** pick one from **tiny.cc/nyhima → documents** — a real, dense HIM
document. Pick the one your Round 1 finding raises a question about.

**What you say:**

"Take what you found in Round 1. One finding — something that surprised you,
something you now have a question about. Choose the document that speaks to it.
Tell the model your story. Ask it what your story means in the context of that
document. Then read what comes back like a professional, not a reader."

**The core prompt — this is the whole instruction:**

> *"Here's the data story I found in Round 1. Tell me what this story means in the
> context of this document."*

"That's it. You're not asking it to summarize the document — you did the reading
in Round 1. You're asking it to *apply* the document to what you found. Then you
judge whether the answer is professionally adequate, and where it needs your
expertise to complete."

**You have 25 minutes. Go.**

*[Facilitator — what's in the document library, so you can steer people: Model
Business Associate Agreement; Breach Notification Rule; Information Blocking
Exceptions; 42 CFR § 482.24 (the CoP for medical records); ICD-10-CM POA + HRRP
conditions excerpt; HIPAA Policy Manual. A readmissions finding points to the BAA
or the HIPAA Manual; an HAI finding to the Breach Rule or the BAA; a PSI finding
to the ICD-10 excerpt; a complications finding to 42 CFR § 482.24; a maternal
health finding to the HIPAA Manual's right-of-access section. You don't need to
say this — just steer if someone is stuck on which document fits.]*

---

# SLIDE 12 — ROUND 2: HOW IT WORKS
*(leave on screen during the round)*

**Interpret — read, think, write with text**

```
1. FIND     Take your Round 1 finding. One story. One number that surprised you.
2. CHOOSE   Pick the document from the library that speaks to it.
3. TELL     "Here's what I found. What does this mean in the context of this document?"
4. EVALUATE Read the output as a professional. Where is the model right?
            Where does it need your expertise to complete?
5. SAVE     Run the workbench prompt. Share your Gemini link in your row.
```

*The document is what only your expertise can fully supply meaning to. The model
applies the framework. You decide whether the application holds.*
*Ahead of the room? Open a second model, paste the same finding and document, ask:*
*"A colleague interpreted this for me. What did they miss?"*

---

# SLIDE 13 — ROUND 2: DEBRIEF

**A model that sounds authoritative about the law is a specific kind of dangerous.**

- If you didn't already know this regulation, how would you know it got it wrong?
- Would you hand the model's version to a colleague without editing it?

> The model applied the framework correctly and reached the wrong conclusion.
> Why? That's the question. And you're the only one in this room who can answer it.

**The debrief question:**

> *What did the model explain correctly — and what did it need your expertise to
> complete?*

---

# SLIDE 14 — ROUND 3: ITERATE
*(25 min · self-directed · your linked story)*

> ## Iterate until it's yours

**What you say:**

"Look at what you have now. Not one thing — a chain. A finding from the data, and
an interpretation of what it means against a real regulation. That's a story with
two parts that belong together. Round 3 is where you make it one piece, and make
it yours.

Take it — the finding and the interpretation — and hand it back to the model. We're
not fixing facts now. We're fixing *voice* and *shape*. Does this read like you made
a call, or like you're hedging? Does the data finding actually connect to what the
regulation says, or are they sitting next to each other? Push back. Run it again.
Then again. Stop when it reads like something you'll put your name on.

And if your chain didn't come together — if the finding and the document never
really connected — you have another move. Go back. Pick a different finding, or a
different document, and run the whole loop again: interrogate, interpret, iterate.
The chain is yours to rebuild. A story that doesn't hold is worth abandoning for
one that does."

**You have 20 minutes. Go.**

---

# SLIDE 15 — ROUND 3: HOW IT WORKS
*(leave on screen during the round)*

**Iterate — read, think, write on your own linked story**

```
TWO PATHS — pick one:

A) Iterate the chain you built
   1. BRING    Paste both pieces back in — your Round 1 finding AND your Round 2
               interpretation. They're one story now.
   2. THINK    "Does this read like a decision or a hedge? Does the finding
               actually connect to what the document says?"
   3. WRITE    "Make the connection explicit. Make it sound like I own this." Run it.
               Push back. Again. One pass is not iteration.
   4. SAVE     Run the workbench prompt. Share your Gemini link in your row.

B) Re-run the whole loop
   Your chain didn't hold? Go back to Round 1. Pick a different finding or a
   different document. Interrogate → Interpret → Iterate, faster this time.
   You know the moves now. Land on a story that holds — then run path A on it.
```

*The back-and-forth is the point. A finding and an interpretation that don't talk
to each other aren't a story yet — iteration is what connects them.*

---

# SLIDE 16 — ROUND 3: DEBRIEF

**Would you put your name on the final version?**

- Where did pushing back actually change the voice — or tighten the connection
  between the finding and the document?
- Where did the model just agree with you?
- Did anyone abandon their first chain and rebuild? What made the second one hold?

> You iterated until it read like something you'll put your name on. That's the
> move that makes a finding-plus-interpretation into one piece of work that's yours.

*[Facilitator note: the source for "would you put your name on it" is the Learner's
Permit, Exercise 13 — "Did You Learn Your Own Slop?" The sharper version of the
question is: did you generate without learning? The conceptual anchor is LP Phase
III citation discipline — every artifact carries name, date, model, and transcript
link. Putting your name on it is not a formality; it's the accountability the whole
day builds toward. Drop the LP framing in if the room is ready for it.]*

---

# SLIDE 17 — IF YOU'RE AHEAD: TWO ENCORES
*(only for tables that finish early — not required)*

**Encore A — Judgment.** Pick a scenario in **tiny.cc/nyhima → judgment** (J1–J4).
These are labeled *"a harder version of what you did today"* — and they are.
*Write your position first — what should happen and why — before you open the
model.* Then make the model argue against you. Watch it perform balance when you
needed a call. (That posture — write your position before opening the model, then
bring it for challenge — is exactly the Learner's Permit Phase III posture. Name
that if it lands.)

**Encore B — The Documentation Gap.** Bring **both** a data file and a document
together from the start. Interrogate the data (where are we failing?), interpret
the document (what does it require?), iterate toward a one-page memo to your CEO
that names the gap and recommends three actions. This is the full chain with the
stakes turned up.

> Real work is never just data or just text. It's both — and it takes all three
> moves to get to something worth acting on.

---

# SLIDE 18 — WRAP: THE META-MOMENT
*(15 min)*

**What you do:**

"Everyone got their link into the shared doc? Watch this."

Pull the shared links, compile them on the projector, and show the room their own
work, side by side.

> ## AI just read everything you produced today.

**What you say:**

"Here's what thirty of you made in three hours. Same five files, different stories.
Same documents, different reads. I just used AI to read all of your AI work — in
about thirty seconds.

So — who gets credit for this?

The model interrogated, interpreted, helped you iterate. *You* decided which
questions mattered, what the document actually meant, and when the chain held
together. The model did none of that. You did."

*(The Morrisville frame: "AI did the work — can I get credit for it?" Let the
question sit. Don't answer it. They already know.)*

---

# SLIDE 19 — CLOSE

> ## It is worth exactly what you put into it.

A vague prompt gets a vague answer. A document you didn't read gets a summary you
can't trust. A real question, real expertise, and the patience to iterate — that
gets you something you can use.

You proved it today. You built one connected thing — a finding, interpreted,
made yours. You're holding the proof.

The AI already in your workflows — the kind that flags and suggests before you've
formed a view — that one's harder to interrogate. But now you have a practice for
it. You know what to ask. You know "the AI said so" isn't an answer. That's not
getting used to it. That's having agency over it.

**Stay in touch:**
- Folder stays live — **tiny.cc/nyhima**
- SUNY Poly AIX Center — sunypolyaix.github.io
- steve@sunypoly.edu

*If time: "One thing you'll do differently Monday?" Let it sit ten seconds. Close.*

---

# APPENDIX A — FACILITATOR PREP CHECKLIST
*(do these before June 7 — not on screen)*

**Pre-build (materials):**
- [ ] **[EXTRACT]** ICD-10-CM POA + HRRP conditions excerpt → `icd-10-poa-and-hrrp-conditions-excerpt.md` (target 8–15 pages; POA section is the operative one).
- [ ] **[CONVERT]** All Round 2 documents to .md for the Drive folder so Gemini reads them without PDF parsing issues. (42 CFR is already plain text. HIPAA Policy Manual is back in the directory.)

**Verify (test before the room):**
- [ ] **[VERIFY]** Gemini share links are public without login — **the meta-moment depends on this.** Test first.
- [ ] **[VERIFY]** Gemini free: CSV upload + chart generation still works on the files you'll hand out.
- [ ] **[VERIFY]** "Show me only the New York hospitals" — confirm what Gemini does with the national file (this is a Round 1 literacy moment; know the failure mode before participants hit it).

**Build / set up:**
- [ ] **[DOWNLOAD]** All five CMS files from their dataset Export buttons (IDs below). **National, not pre-filtered to NY** — filtering is itself a Round 1 prompt with a real failure mode.
- [ ] **[BUILD]** Shared Google Doc — numbered rows, instructions at top: "Find your number. Paste your link as you go. Don't edit other rows."
- [ ] **[PRINT]** Numbered cards for the door.
- [ ] **[SETUP]** tiny.cc/nyhima → folder with the five data files, the document library, system prompts, this run of show.
- [ ] **[RECRUIT]** One helper to circulate during rounds. Get there early.

**Round 1 data files — download from the Export button on each dataset page:**

| File | CMS Dataset ID | Dataset page |
|------|----------------|--------------|
| Complications_and_Deaths-Hospital.csv | ynj2-r877 | data.cms.gov/provider-data/dataset/ynj2-r877 |
| FY_2026_Hospital_Readmissions_Reduction_Program_Hospital.csv | 9n3s-kdb3 | data.cms.gov/provider-data/dataset/9n3s-kdb3 |
| CMS_PSI_6_decimal_file.csv | muwa-iene | data.cms.gov/provider-data/dataset/muwa-iene |
| Healthcare_Associated_Infections-Hospital.csv | 77hc-ibv8 | data.cms.gov/provider-data/dataset/77hc-ibv8 |
| Maternal_Health-Hospital.csv | nrdb-3fcy | data.cms.gov/provider-data/dataset/nrdb-3fcy |

*Hash-based CDN URLs change with each CMS data refresh — use the Export button, not a copied link. Keep `cms-hospital-data-synthesis.md` open during the Round 1 debrief; do not give it to participants.*

---

# APPENDIX B — WHAT CHANGED FROM v5

- **Round 1 names the five data files** and gives a reason to pick each (sourced
  to `cms-hospital-data-synthesis.md`). Replaces the single "New York hospital file."
- **Data is national, not pre-filtered to NY.** "Show me only New York hospitals"
  is now itself a Round 1 prompt with a catchable failure mode.
- **New facilitator-only slide (10b):** the five things the model will get wrong —
  debrief ammunition, not on screen.
- **Round 1 debrief (Slide 10):** the single placeholder lesson line is replaced by
  three framings keyed to what happens at the tables, plus the grounded-theory frame.
- **Round 2 redesigned around the data story.** The instruction is now one sentence
  — *"Here's the data story I found in Round 1. Tell me what this story means in the
  context of this document."* The task is application, not compression. The HIPAA
  Policy Manual is back in the document library alongside the BAA, Breach Notification
  Rule, Information Blocking Exceptions, 42 CFR § 482.24, and the ICD-10-CM excerpt.
- **Round 2 debrief (Slide 13):** keeps the "authoritative about the law is dangerous"
  line; adds the "applied the framework correctly, reached the wrong conclusion" turn
  and the new debrief question.
- **Round 3 rebuilt on the linked artifacts.** Iteration now operates on the
  finding-plus-interpretation as one story, not a stray draft — with a second path
  to re-run the whole Interrogate → Interpret → Iterate loop if the chain didn't hold.
- **"Put your name on it"** replaces "sounds like you wrote it" throughout (Slides 2,
  5, 16). Slide 16 facilitator note now points to LP Exercise 13 and Phase III
  citation discipline.
- **Agency-not-adaptation** stated in the overview and carried to the close; a new
  Slide 4 ("Why this, why now") names the directive-AI stakes without lecturing.
- **The three rounds are framed as one chain** in the overview, the spine slide, and
  the lightning round.

---

# APPENDIX C — WHAT CHANGED FROM v3
*(carried forward from v5 for the record)*

- Spine renamed **Interrogate / Interpret / Iterate** (was Data / Text / Validation).
- **Round 3 is Iteration, not Validation** — tone and ownership, not "is it sound?"
- Icebreaker teaches **"I am…" not "You are…"** (audience prompt, not role prompt).
- Round 2 simplified to **one model + one shared link**; the second-model check is an
  *ahead-of-the-room* option, not a required step.
- **Two encores** added for fast tables (Judgment; The Documentation Gap).
- Wrap rebuilt around the **live meta-moment** + the Morrisville credit question.
- Participants identified by **number → row**, no separate handout.

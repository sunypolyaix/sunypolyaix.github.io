---
id: facilitator-deck
type: facilitator
title: Reading and Writing with AI — Facilitator Deck (v7)
event: NYHIMA Workshop
date: June 7, 2026 | 1:00–4:00 PM
presenter: Steve Schneider, SUNY Poly AIX Center
structure: lightning + three rounds (Interrogate / Interpret / Iterate)
parent: nyhima-facilitator-deck-v6.md
revision_notes: nyhima-v6-notes-001.md, nyhima-v6-notes-002.md
status: v7 — opening reframed as three I's; Gemini window slide added; workbench and shared doc removed; document library fixed to four; 25/100/400 Round 3
---

# Reading and Writing with AI
## Facilitator Deck — v7
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

Today asks **how.** What is left unasked is **why** — why you'd do this, what it costs, what it's for. The how comes first. You can't answer the why without knowing the how.

The frame for the whole day is **agency, not adaptation.** Not "AI is here, get
used to it" — "AI is here, and you have agency over it." Every participant in this
room works in healthcare. The systems we are asking them to exercise judgment over
moved fast and arrived before most professional training caught up. That weight
deserves acknowledgment, not cheerleading. The work is real because the stakes are.

Base path is dead simple: one model, one chain. Everything richer (a second model,
the encores) is optional, for tables that are ahead. When in doubt, keep the room
on the simple path.

---

## Run of show

| Segment | Time | Cumulative |
|---------|------|------------|
| Opening | 10 min | 1:10 |
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

---

# SLIDE 2 — OPENING
*(10 min · start without slides — just talk)*

**What you say:**

"Good afternoon. Thank you for joining our workshop, which is focused on using
artificial intelligence tools — today, just large language models — to do your work.

On Tuesday in a breakout session we'll frame some questions about why you might
want to do this, at what cost to you, to the world, to the environment, to your
organization. But today we're going to focus on reading, thinking, and writing.
If Tuesday is the why or why not, today is the how.

We do that in three moves. We'll **interrogate** data — upload a file, ask it
questions, surface a story. Then we'll **interpret** text — take that finding into
a real regulatory document and ask what it means. Then we'll **iterate** our work
— take the result and reshape it until it reads like something you actually believe.

But here's the thing. At every step, the model produces output. Your job is
deciding whether that output is any good. It will sound authoritative. It will be
confidently wrong sometimes. It won't flag its own mistakes. You have to.

So today you're not learning to use AI. You're learning to think with it — and to
know exactly when not to trust it. That's the actual skill."

**What you don't say:**
- Don't explain what a transformer is. They don't need it.
- Don't apologize for the tech. If it breaks, that's data.

Today asks how. What is left unasked is why.

---

# SLIDE 3 — ICEBREAKER + INFRASTRUCTURE
*(20 min)*

> ## Open tiny.cc/nyhima

**What you say:**

"Open that on your laptop or tablet. Everything you need today lives there — the
data files, the document library, the system prompts, this reference card.

While you're getting in: open Gemini at gemini.google.com. Free account, no
install. That's your primary tool today."

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

**Browser skills we assume:**

- Open a new tab
- Navigate between tabs
- Copy text (Cmd/Ctrl+C) and paste (Cmd/Ctrl+V)
- Download a CSV file from a link and upload it to Gemini
- Find a file you just downloaded

**By the end of today you will have four tabs open:**

| Tab | What's in it |
|-----|--------------|
| 1 | tiny.cc/nyhima — your materials hub |
| 2 | Gemini — Round 1 conversation |
| 3 | Gemini — Round 2 conversation |
| 4 | Gemini — Round 3 conversation |

*Each round gets its own conversation. Clean context. Fresh start.*

---

# SLIDE 4 — THE GEMINI WINDOW
*(use the icebreaker response to walk through this — point to the buttons as you go)*

**What you say:**

"Look at the response we just got. See the buttons under it. Each one tells you
something about what this thing actually is."

**The four buttons — and what they mean:**

| Button | What it does | What it teaches |
|--------|--------------|-----------------|
| **Thumbs up / Thumbs down** | Sends feedback to Google | Both things likely happen: it shapes this conversation, and it feeds into future Gemini training. You're putting a signal into the system. Experiment with it. |
| **Copy** | Takes the response to your clipboard | The transcript stays in Gemini — but copying makes it portable. You're moving it into your space, your document, your control. |
| **Open in Google Docs** | Sends the response directly into a Google Doc | Skips copy/paste. Puts model output into a collaborative context where real work happens. |
| **Regenerate** | Asks the model to answer the same prompt again, differently | There is no single right answer. The model picked one likely next word, then another. Ask again — you get a different path through the same probability space. |

"That last button — Regenerate — is the most important thing I can show you about
what a language model is. It's not retrieving a fact. It's generating a probable
response. That's why your judgment matters. Every single time."

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

"Five files. All real, all national. Each one asks a different question about hospitals.
Here's the question each file is designed to answer. Pick the file that fits work
you actually do."

**Start every file with this prompt:**

> *"Tell me what's in this dataset. What is the unit of analysis — what does each
> row represent? How many hospitals are in here? What are the key metrics?
> What data is missing or marked unavailable?"*

That's your data dictionary. Get that first. Then ask your question.

**The five files and their questions:**

| File | The question |
|------|-------------|
| **Complications & Deaths** | How do documentation practices and hospital type explain differences in mortality rates across diseases? |
| **Hospital Readmissions (HRRP)** | How do readmission prevention programs and hospital type explain differences in readmission rates across conditions? |
| **Patient Safety Indicators (PSI-6)** | How do procedural volumes and hospital type explain differences in adverse event rates? |
| **Healthcare-Associated Infections (HAI)** | How do infection prevention protocols and hospital type explain differences in infection rates? |
| **Maternal Health** | How do prenatal screening practices and hospital type explain differences in maternal health outcomes? |

"Upload your file. Run the data dictionary prompt first. Then ask your question.
The model reads faster than you can — but it only finds what you think to ask for,
and it won't flag what it gets wrong. That's your job. Hold onto one finding.
You'll carry it into Round 2."

**You have 25 minutes. Go.**

---

# SLIDE 9 — ROUND 1: HOW IT WORKS
*(leave on screen during the round)*

**Interrogate — read, think, write with data**

```
1. Open a new Gemini tab. Upload your file.
2. Run the data dictionary prompt: "What is each row? How many hospitals?
   What are the key metrics? What's missing?"
3. Ask your three-variable question.
4. Push one level deeper — "What kind of hospital is the outlier?"
5. Note your one finding — the number or pattern you're carrying to Round 2.
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

*[Facilitator — four documents in the library, one primary pairing per data file:
42 CFR § 482.24 → Complications & Deaths, Maternal Health;
Business Associate Agreement → HRRP;
Breach Notification Rule → HAI;
ICD-10-CM POA excerpt → PSI-6 Decimal.
Steer if someone is stuck — don't announce the pairings up front.]*

---

# SLIDE 12 — ROUND 2: HOW IT WORKS
*(leave on screen during the round)*

**Interpret — read, think, write with text**

```
1. Take your Round 1 finding. One story. One number that surprised you.
2. Pick the document from the library that speaks to it.
3. "Here's what I found. What does this mean in the context of this document?"
4. Read the output as a professional. Where is the model right?
   Where does it need your expertise to complete?
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
*(25 min · self-directed)*

> ## 25 words. 100 words. 400 words.

**What you say:**

"You have a finding and an interpretation. Now make it usable.

Paste your Round 2 output back in. Ask for 25 words. Read what comes back — that's
the model's version of what you actually argued. If it's wrong, that's where you
push back. Not on the 400-word version. On the 25.

When the 25-word version is right, ask for 100. That's who you're writing for — it
forces the audience question. Then 400. That's the thing you'd send.

If you need a different register — for a physician, for a board, for a patient —
ask for that too. Same finding, different voice. That's the move."

**You have 20 minutes. Go.**

---

# SLIDE 15 — ROUND 3: HOW IT WORKS
*(leave on screen during the round)*

```
1. Paste your Round 2 output back in.
2. "Write this as 25 words."
3. Read it. Is that your argument? If not, fix it here — not later.
4. "Now write it as 100 words."
5. "Now write it as 400 words."
6. Optional: "Rewrite this for [specific audience — physician / board / patient]."
```

*The 25-word version is the test. If you can't say it in 25 words,
you don't know what you're arguing yet.*

*Ahead of the room? Paste the 25-word version into a second model.
Ask it to expand to 400. Compare the two.*

---

# SLIDE 16 — ROUND 3: DEBRIEF

**What did the 25-word version reveal?**

- Was the model's 25 words your argument — or its own?
- What did the 400-word version add that earned its place?
- Where did changing the audience change what needed to be said?

> The gap between 25 words and 400 words is where padding lives.
> Your job was to decide what belongs in that gap.

---

# SLIDE 17 — IF YOU'RE AHEAD: TWO ENCORES
*(only for tables that finish early — not required)*

**Encore A — Judgment.** Pick a scenario in **tiny.cc/nyhima → judgment** (J1–J4).
These are labeled *"a harder version of what you did today"* — and they are.
*Write your position first — what should happen and why — before you open the
model.* Then make the model argue against you. Watch it perform balance when you
needed a call.

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

"Who wants to share what they found? Not the model's output — your finding.
One sentence."

Ask two or three people. Each one is a different story from the same data.

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

Today asked how. What's left unasked is why — why you'd do this, what it costs,
what it's for. That's the harder question. But you can't answer it without knowing
how first. And now you do.

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
- [ ] **[CONVERT]** All Round 2 documents to .md for the Drive folder so Gemini reads them without PDF parsing issues. (42 CFR is already plain text.)

**Verify (test before the room):**
- [ ] **[VERIFY]** Gemini share links are public without login — **the meta-moment depends on this.** Test first.
- [ ] **[VERIFY]** Gemini free: CSV upload + chart generation still works on the five data files.
- [ ] **[VERIFY]** "Show me only the New York hospitals" — confirm what Gemini does with the national file (this is a Round 1 literacy moment; know the failure mode before participants hit it).

**Build / set up:**
- [ ] **[DOWNLOAD]** All five CMS files from their dataset Export buttons (IDs below). **National, not pre-filtered to NY** — filtering is itself a Round 1 prompt with a real failure mode.
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

# APPENDIX B — WHAT CHANGED FROM v6

- **Opening reframed as three I's.** "Good afternoon" opening, how vs. why frame, interrogate/interpret/iterate named explicitly as the through-line.
- **Slide 4 replaced.** "Why this, why now" → "The Gemini Window" — four buttons, what each teaches about what the model is. Regenerate is the key lesson.
- **Browser skills added to Slide 3.** Four-tab end state named explicitly.
- **Workbench prompt removed entirely.** No workbench prompt in any round.
- **Shared doc and numbered cards removed.** Both optional in Appendix A.
- **Document library fixed to four.** BAA, Breach Notification Rule, 42 CFR § 482.24, ICD-10-CM POA excerpt. IB Exceptions and HIPAA Policy Manual out.
- **Round 3 rebuilt as 25/100/400.** Iteration now operates on length and register, not a vague "push back."
- **Slide 1 cleaned.** Doubled line removed.
- **Slide 19 close** carries the how/why frame explicitly.

---

# APPENDIX C — WHAT CHANGED FROM v5
*(carried forward for the record)*

- Spine renamed **Interrogate / Interpret / Iterate** (was Data / Text / Validation).
- **Round 3 is Iteration, not Validation** — tone and ownership, not "is it sound?"
- Icebreaker teaches **"I am…" not "You are…"** (audience prompt, not role prompt).
- Round 2 simplified to **one model**; the second-model check is an *ahead-of-the-room* option.
- **Two encores** added for fast tables (Judgment; The Documentation Gap).
- Wrap rebuilt around the **live meta-moment** + the Morrisville credit question.

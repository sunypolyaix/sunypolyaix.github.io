# Reading and Writing with AI
## Facilitator Deck — NYHIMA Workshop | June 7, 2026 | 1:00–4:00 PM

---

## SLIDE 00 — Title / Holding Slide
*(on screen as participants arrive)*

**Reading and Writing with AI**
Using Large Language Models in Professional Practice

Steve Schneider | SUNY Poly AIX Center
NYHIMA | June 7, 2026

Everything lives at: **tiny.cc/nyhima**

---

## SLIDE 01 — Opening Question
*(10 min | no slides until now — just talk)*

**Who prompted that?**

Think about the last time AI showed up in your work—not something you went looking for.

- A recommendation
- A flagged record
- A suggested code
- A pre-populated field

*Who asked for it?*

---

## SLIDE 02 — What You'll Build Today

Three sprints. Real HIM scenarios. At least two models.

By 4:00 PM you have artifacts you generated, saved, and can take back to your organization.

**That's your workbench. It's yours.**

---

## SLIDE 03 — Get Connected
*(Icebreaker + Infrastructure | 20–25 min)*

**Open: tiny.cc/nyhima**

You need:
- A laptop or tablet
- **At least two** of these open: ChatGPT, Claude, Gemini
- A browser. That's it.

*Table captains: help your neighbors get in.*

---

## SLIDE 04 — Icebreaker Prompt
*(leave on screen while they run it)*

Open **both** models. Paste this into each:

> *You are an expert in health information management. In exactly one sentence, describe what HIM professionals do—written for a hospital board member who has never heard the term.*

Read both outputs. **Are they the same?**

---

## SLIDE 05 — What You Just Saw

Same prompt. Different models. Different outputs.

**The model is a variable, not a constant.**

This matters. We'll come back to it.

---

## SLIDE 06 — System Prompts
*(leave on screen during demo)*

A system prompt is your first message — it tells the model how to behave before you ask your real question.

| Code | Name | Use for |
|------|------|---------|
| SP-01 | Skeptical Reviewer | Any validation task |
| SP-02 | Plain Language Translator | Policy writing |
| SP-03 | Devil's Advocate | Judgment bucket |
| SP-04 | Executive Communicator | Data writing |
| SP-05 | Patient Advocate | Judgment validation |
| SP-06 | Neutral Summarizer | Moving outputs between models |

Full prompts: **tiny.cc/nyhima → system-prompts/**

---

## SLIDE 07 — The Day's Structure

Three sprints. Each one asks more of you than the last.

| Sprint | Bucket | The task | What you learn |
|--------|--------|----------|----------------|
| 1 | Data | Two models, one prompt | More models catches more |
| 2 | Policy | One model, multiple prompts | Iteration improves output |
| 3 | Judgment | Both strategies + your reasoning first | You get out what you put in |

---

## SLIDE 08 — Sprint 1: Data
*(35 min | 25 sprint + 10 debrief)*

**Pick any scenario in Bucket D**

| ID | Title |
|----|-------|
| D1 | The Discharge Data |
| D2 | The Coding Accuracy Audit |
| D3 | The ROI Request Surge |
| D4 | The Duplicate MRN Problem |

*tiny.cc/nyhima → scenarios/data/*

**You have 25 minutes. Go.**

---

## SLIDE 09 — Sprint 1: How It Works
*(leave on screen during sprint)*

**Sprint 1 — Two models, one prompt**

```
1. Read the situation
2. Paste the source into Model A
3. Run the writing prompt → save the output
4. Switch to Model B
5. Paste the validation prompt + Model A's output
6. Compare — what did Model B catch?
```

**Try:** SP-04 (Executive Communicator) on Model A
**Try:** SP-01 (Skeptical Reviewer) on Model B

*Finished early? Run the same scenario with models swapped.*

---

## SLIDE 10 — Sprint 1 Debrief

**Did the second model catch something the first one missed?**

- Did both models agree — and were they both wrong?
- Where did your own knowledge have to step in?

> One prompt, one model is the floor.
> Two models plus your expertise is the point.

---

## SLIDE 11 — Sprint 2: Policy
*(35 min | 25 sprint + 10 debrief)*

**Pick any scenario in Bucket P — work in pairs**

| ID | Title |
|----|-------|
| P1 | The Information Blocking Rule |
| P2 | The Minimum Necessary Standard |
| P3 | The Retention Policy Gap |
| P4 | The Breach Notification Clock |

*tiny.cc/nyhima → scenarios/policy/*

**You have 25 minutes. Go.**

---

## SLIDE 12 — Sprint 2: How It Works
*(leave on screen during sprint)*

**Sprint 2 — One model, multiple prompts**

```
1. Read the situation
2. Paste the source into your model
3. Run the writing prompt → read the output
4. Push back — what did it miss? what's soft? run it again
5. Refine at least once more
6. Now run the validation prompt — is the final version better?
```

**Try:** SP-02 (Plain Language Translator) to start
**Try:** SP-01 (Skeptical Reviewer) to pressure-test your best version

*Stuck? P4 (Breach Notification) generates the most friction. P2 (Minimum Necessary) is the most immediately practical.*

---

## SLIDE 13 — Sprint 2 Debrief

**Did the output get better when you pushed back?**

- What did you have to know to push back at all?
- Would you hand the final version to a colleague without editing it?

**If you didn't already know this regulation, how would you have known the model got it wrong?**

*A model that sounds authoritative about law is a specific kind of dangerous.*

---

## SLIDE 14 — Sprint 3: Judgment
*(35 min | 25 sprint + 10 debrief)*

**Pick any scenario in Bucket J — work as a full table**

| ID | Title |
|----|-------|
| J1 | The Physician Who Won't Document |
| J2 | The Record Request That Worries You |
| J3 | The AI Note in the Chart |
| J4 | The Vendor Who Wants Your Data |

*tiny.cc/nyhima → scenarios/judgment/*

**Before you open a model: stop.**

---

## SLIDE 15 — Sprint 3: Before You Touch the Keyboard

Read the scenario. Then:

**Open a Google Doc. Write 2–3 sentences: what do you think should happen?**

Your position. Your reasoning. Your call. Keep the doc open — you'll need it at the end.

*Then* open the model.

---

## SLIDE 16 — Sprint 3: How It Works
*(leave on screen during sprint)*

**Sprint 3 — Your reasoning first, then both strategies**

```
1. Write your position before you prompt (Slide 15)
2. Build that reasoning into your opening prompt
3. Run it in Model A → push back → refine at least twice
4. Take your best output to Model B
5. Have Model B stress-test it
6. Paste your original sentences from the Google Doc into the model — ask it to critique your reasoning. Where were you wrong? What did you miss?
```

**Try:** SP-03 (Devil's Advocate) or SP-05 (Patient Advocate) on Model B

*J3 (AI Note in the Chart) and J4 (Vendor Data) generate the strongest table discussion.*

---

## SLIDE 17 — Sprint 3 Debrief

**Did the output get better every time you pushed?**

- Where did your reasoning make the model's response sharper?
- Where did the model perform balance instead of taking a side?
- Would you put your name on the final output?

> You get out what you put in.
> The people reading your work can feel when you phoned it in.

---

## SLIDE 18 — Wrap
*(10–15 min)*

**Who prompted that?**

You've spent three hours on the version where you do the prompting.

Sprint 1: more models catches more.
Sprint 2: more prompts, better output.
Sprint 3: your thinking is the input that makes it worth anything.

The AI already in your workflows did none of that work for you. It surfaced something before you had a position. Now you know what that costs.

---

## SLIDE 19 — What You Built

Whatever you saved today is yours.

- Artifacts you generated
- Refinements you pushed through
- Your judgment about where the model earned it and where it didn't

**Lightweight. Portable. The start of a practice.**

12 scenarios total. Three buckets. The rest are at tiny.cc/nyhima when you want them.

---

## SLIDE 20 — The One Thing

> **It is worth exactly what you put into it.**
> **And the people reading your work can feel it.**

---

## SLIDE 21 — Close
*(stay on screen through Q&A)*

**tiny.cc/nyhima** — Drive folder stays live

SUNY Poly AIX Center: **sunypolyaix.github.io**

Questions, follow-up, collaboration: **steve@sunypoly.edu**

---
*What's one thing you're going to do differently on Monday?*

---

## APPENDIX: Timing Guide

| Segment | Duration | Clock |
|---------|----------|-------|
| Opening | 10 min | 1:10 |
| Icebreaker + Infrastructure | 25 min | 1:35 |
| Sprint 1: Data | 35 min | 2:10 |
| Sprint 2: Policy | 35 min | 2:45 |
| Sprint 3: Judgment | 35 min | 3:20 |
| Wrap | 15 min | 3:35 |
| Buffer | 25 min | 4:00 |

---

## APPENDIX: Sprint Structure Summary

| Sprint | Models | Prompts | Your input | Lesson |
|--------|--------|---------|------------|--------|
| 1 — Data | Two | One | Evaluation | More models catches more |
| 2 — Policy | One | Multiple | Pressure | Iteration improves output |
| 3 — Judgment | Two | Multiple + refinement | Your reasoning first | You get out what you put in |

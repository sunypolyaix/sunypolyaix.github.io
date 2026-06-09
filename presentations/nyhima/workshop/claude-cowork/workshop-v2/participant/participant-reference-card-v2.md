---
id: handout
type: participant
title: Workshop Reference Card (v2)
---

# Reading and Writing with AI
## NYHIMA Workshop — June 7, 2026 | Steve Schneider, SUNY Poly AIX Center

---

## Everything lives here
**tiny.cc/nyhima** → exercise sheets + document library + system prompts + this card

---

## Two rounds

| Round | What you work with | Model to use |
|-------|--------------------|--------------|
| **Round 1 — Data** | A real CMS dataset of New York hospitals | **Gemini (free)** — it can do math on a file you upload |
| **Round 2 — Text** | A dense HIM document you choose | **Claude or ChatGPT (free)** — strong with text, plus a second model to check the first |

---

## The cycle for each round

**Round 1 — Data (one model, three moves):**

1. **Read** — upload the data and ask what is in it
2. **Think** — pick a story the data could tell
3. **Write** — produce a one-page memo with a chart
4. **Workbench** — run the workbench prompt and save it

**Round 2 — Text (two models):**

1. **Read** — paste the document, ask for a plain-language summary
2. **Think** — work out what matters and where the traps are
3. **Write** — produce the artifact (guidance, checklist, memo)
4. **Check** — open a second model and ask it to find what the first missed
5. **Workbench** — run the workbench prompt and save it

---

## The workbench prompt — the most important prompt today

Run this at the end of **every** round. Copy it exactly:

> **Generate a markdown summary of what we did here, starting with my first
> prompt. Identify the questions I asked and how we arrived at the final
> product. Include the final artifact verbatim. I want to copy this into a
> Google Doc to share with colleagues.**

It turns your scattered chat into one clean document — your prompts, the
reasoning, and the finished product — that you can paste into a Google Doc and
share.

---

## Round 2 — checking with a second model

After the first model writes your artifact, open a different model, paste the
artifact, and ask **one** simple question:

> A colleague summarized this for me. Here it is. What did they miss?

> Is this right?

Where the two models disagree is where your judgment goes to work.

---

## System prompts (short version)

Paste one as your first message to change how a model behaves.

| Code | Name | Use for |
|------|------|---------|
| SP-01 | Skeptical Reviewer | Round 2 — checking the first model |
| SP-02 | Plain Language Translator | Round 2 — writing for non-experts |
| SP-04 | Executive Communicator | Round 1 — the leadership memo |
| SP-06 | Neutral Summarizer | Moving an artifact between models |

Full prompts: **tiny.cc/nyhima → system-prompts**

---

## Saving your work

**Easiest:** run the workbench prompt, then paste the result into a Google Doc.

**Also good:** download the conversation.
- ChatGPT: Settings → Data Controls → Export
- Claude: conversation menu → Export
- Gemini: limited export; copy manually

**The point:** you leave with a file, not a browser tab.

---

*SUNY Poly AIX Center | sunypolyaix.github.io | steve@sunypoly.edu | tiny.cc/nyhima*

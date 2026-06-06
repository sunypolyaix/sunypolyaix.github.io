---
title: NYHIMA Workshop Sprint Redesign and J Prompts
date: 2026-06-02
type: conversation
status: reference
project: nyhima-workshop
contributor: Steve
tags: [nyhima-workshop, ai-rtw, workshop-design, sprint-structure, j-bucket, facilitator-deck]
source: claude-conversation
artifacts_produced:
  - nyhima-facilitator-deck.md
  - J1-physician-documentation.md
  - J2-patient-access-safety.md
  - J3-ai-generated-note.md
  - J4-vendor-data.md
decisions_made:
  - Dropped compositional/directive framing entirely from workshop — opens with "who prompted that?" and lets wrap land on its own
  - Three-sprint structure redesigned around a single spine: more models (Sprint 1) → iteration (Sprint 2) → your reasoning first + both strategies (Sprint 3)
  - Sprint 1 — Data: two models, one prompt; compare outputs; second model critiques first
  - Sprint 2 — Policy: one model, multiple prompts; at least one refinement cycle built in; human evaluates, not a second model
  - Sprint 3 — Judgment: participant writes position in Google Doc first; brings reasoning into prompt; multiple refinements; second model stress-tests; final move is pasting original sentences back for model critique
  - J bucket writing prompts rewritten to assume participant brings a position — "help me think through" framing replaced with [paste your sentences] slot
  - Workshop requires at least two models open (ChatGPT, Claude, Gemini — pick 2 or all 3)
  - Closing line set as "It is worth exactly what you put into it — and the people reading your work can feel it"
open_questions:
  - Participant reference card not yet revised to reflect new sprint structures
  - Level-set slide (Mentimeter/Excel survey) not yet designed — survey questions and live display approach TBD
next_actions:
  - Revise participant reference card to match new sprint structures and Google Doc instruction
  - Design level-set survey slide and confirm survey instrument
  - Test J bucket writing prompts — confirm [paste your sentences] slot is clear to a participant reading cold
linked_notes:
  - notes/2026-06-02-output-worth-input.md
---

Session redesigned the three-sprint structure of the NYHIMA Sunday workshop (June 7, 2026) and rewrote all four Judgment bucket writing prompts. Core decision: each sprint isolates one variable — breadth, iteration, effort — so the three-hour arc builds toward Sprint 3 as the full practice. The compositional/directive distinction was dropped entirely; the workshop now opens without framing and closes with an effort-based literacy claim. Facilitator deck revised to 21 slides with three distinct working slides (one per sprint) designed to stay on screen during participant work. J bucket prompts restructured so participants write their position in a Google Doc before touching the model, then build that reasoning into the prompt, then receive the model's critique of their own thinking as the final move. Participant reference card remains to be revised.

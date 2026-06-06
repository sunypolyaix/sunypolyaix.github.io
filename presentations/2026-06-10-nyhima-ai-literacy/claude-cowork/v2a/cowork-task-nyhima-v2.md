# Cowork Task: NYHIMA Workshop + Talk Full Build-Out
## Date: 2026-06-02 | Project: nyhima-workshop

---

## Context — Read These First

Before starting, read:
1. `/mnt/user-data/outputs/conversations/steve/nyhima-workshop/2026-06-02-sprint-redesign.md`
2. `/mnt/user-data/outputs/conversations/steve/nyhima-workshop/2026-06-02-workshop-redesign-part2.md`
3. Project files: `00-opening.md` through `05-wrap.md`, all D/P/J scenarios, `system-prompts.md`

---

## GOAL

Build complete materials for:
1. **Sunday June 7 — 3-hour workshop** (Read-Think-Write with AI)
2. **Tuesday June 9 — 1-hour talk** (Why compositional literacy matters for HIM leadership)

---

## WORKSHOP STRUCTURE (locked)

```
Opening                     10 min
Icebreaker + Infrastructure 15 min
Lightning Round (guided)    30 min  ← Steve leads full arc once
Round 1: Data (self-direct) 30 min
Round 2: Text (self-direct) 30 min
Round 3: Validate (self-dir)30 min
Wrap                        15 min
TOTAL                       3 hours
```

**Lightning Round:** Steve guides participants through all three rounds compressed — simple data file, simple text, simple validation — so they see the full arc before doing it themselves.

**Round 1 (Data):** Gemini free. CMS Hospital General Information CSV filtered to New York. Read-Think-Write. Workbench prompt at end.

**Round 2 (Text):** Gemini free. One dense HIM document from document library. Model A reads, produces artifact. Model B (fresh Gemini conversation) critiques with simple prompt. Workbench prompt at end.

**Round 3 (Validation):** Upload Round 1 artifact + Round 2 artifact + original source files to a fresh model (Claude free preferred — 30MB per file, 20 files per conversation). Ask: "I produced these two artifacts using AI. What should I worry about before I hand either of these to my boss?" Workbench prompt at end.

**Primary model throughout:** Gemini free (handles CSV, code execution, charts, native Google Docs sharing)

**Round 3 validation model:** Claude free (TBD — [VERIFY] test file upload limits before workshop)

---

## GOOGLE DRIVE INFRASTRUCTURE

**tiny.cc/nyhima** → shared Google Drive folder containing:
- All participant-facing materials
- Prompt libraries for each round
- System prompts library
- Link to shared Google Doc template (artifact collection)
- Model recommendations by round

**Shared Google Doc template:**
Pre-built rows, one per anticipated participant. Columns:
- Color code (participant identifier — colored cards distributed at door)
- Name (optional — can stay anonymous)
- Round 1 Artifact Link
- Round 1 Gemini Conversation Link
- Round 2 Artifact Link
- Round 2 Gemini Conversation Link
- Round 3 Validation Notes

Build this template as a Google Doc. Include instructions at top: "Find your color. Paste your links as you go. Don't edit other rows."

---

## THE WORKBENCH PROMPT (most important prompt in workshop)

This prompt appears in every round and in the participant reference card:

> *Generate a markdown summary of what we did here, starting with my first prompt. Identify the questions I asked and how we arrived at the final product. Include the final artifact verbatim. I want to copy this into a Google Doc to share with colleagues.*

Give this its own slide in the facilitator deck and its own section in the participant reference card. It is the move that turns a conversation into a workbench.

---

## WHAT TO BUILD

### 1. Facilitator Deck v2
Revise `nyhima-facilitator-deck.md` to reflect new structure. Key slides needed:

- Holding slide (pre-session)
- Opening: "Who prompted that?" — no framing, just the question
- Infrastructure: Gemini free, Google Drive, colored cards, shared Doc
- Icebreaker: run the HIM definition prompt in Gemini, compare outputs
- Lightning Round intro + three working slides (Data / Text / Validation)
- Round 1 working slide (stays on screen during sprint)
- Round 2 working slide
- Round 3 working slide
- Workbench prompt slide (standalone — used at end of every round)
- Wrap: "It is worth exactly what you put into it"
- Close / stay in touch

### 2. Participant Reference Card v2
Single page. Reflects two-round + lightning structure. Contains:
- Model recommendations (Gemini for all, Claude for Round 3 validation)
- Sprint cycle for each round
- Workbench prompt prominently (box it, make it impossible to miss)
- System prompts short table
- Saving your work (Gemini share link + Google Doc)
- tiny.cc/nyhima URL
- Colored card instruction ("find your row in the shared doc")

### 3. Round 1 Exercise Sheet
One-page participant document:
- Model: Gemini free
- Dataset: CMS Hospital General Information — filter to New York
- Download link: `https://data.cms.gov/provider-data/dataset/xubh-q36u`
- Starter prompts:
  - **Read:** "Here is a dataset of New York hospitals from CMS. Summarize the data structure. What patterns do you see?"
  - **Think:** "I want to tell a story about [NY's regional position / star ratings by ownership / quality vs. spending]. Help me think through what the data shows."
  - **Write:** "Generate a memo of no more than one page with a chart that tells this story to my hospital's leadership."
  - **Workbench:** [paste workbench prompt]
- Note: Gemini free handles CSV uploads and chart generation. If you hit token limits, open a fresh Gemini conversation.

### 4. Round 2 Document Library
7 scenario sheets. Each contains:
- Document excerpt (the source text to upload)
- Starter Read prompt
- Starter Think prompt
- Starter Write prompt
- Model B critique prompt: "A colleague summarized this document for me. Here it is. What did they miss?" or "Is this right?"
- Workbench prompt

**Documents:**
- R2-hipaa-minimum-necessary.md (from P2 — revise for new structure)
- R2-information-blocking.md (from P1 — revise)
- R2-breach-notification.md (from P4 — revise)
- R2-vendor-baa.md (new — write realistic fictional BAA excerpt)
- R2-joint-commission-rc.md (new — RC.02.01.01 standard)
- R2-cms-cop-medical-records.md (new — 42 CFR § 482.24 excerpt)
- R2-roi-policy.md (new — fictional hospital ROI policy section)

### 5. Round 3 Exercise Sheet
One-page participant document:
- Instruction: "Upload everything — your Round 1 artifact, your Round 2 artifact, and the original source files — into a fresh Claude conversation."
- The validation prompt: "I produced these two artifacts using AI. Here are the source files I worked from. What should I worry about before I hand either of these to my boss? Where is my reasoning soft? What did I miss?"
- Note on model: Claude free preferred (handles multiple file uploads)
- [VERIFY]: Test Claude free file upload limits before finalizing this sheet

### 6. Workbench Prompt Card
Standalone resource. One prompt, clean formatting, copy-pasteable. Explain what it does and why it matters. Lives in Google Drive folder and prints as a physical card if needed.

### 7. System Prompts Library
Keep existing `system-prompts.md` as-is. Add one new prompt:

**SP-07: Governance Reviewer**
> You are a senior HIM leader evaluating AI-generated work product. Your job is to determine whether this artifact is safe to act on. Identify: what assumptions it makes, what it might have gotten wrong, what professional judgment it requires before implementation, and what your name on this document would mean for your liability.

---

## TALK BUILD-OUT (Tuesday June 9)

### Argument (locked)
Compositional AI literacy (Read-Think-Write) is a credential requirement for HIM leadership, not for individual contributors. The credential levels:
- **Associate / individual contributor:** Uses directive AI (coding suggestions, record flags, workflow recommendations). Does not need compositional literacy.
- **Bachelor / supervisory:** Needs compositional literacy to audit, govern, and train people using directive AI.
- **Master / organizational leadership:** Must have compositional literacy. Makes institutional decisions about AI deployment, governance, policy.

### Framework (locked)
**D-P-J × R-T-W 3×3 matrix** as the visible front skin of the voxel taxonomy.

Rows: Data (D), Policy (P), Judgment (J)
Columns: Read (R), Think (T), Write (W)

Each cell contains voxels along five dimensions:
1. cognitive_mode (read/think/write)
2. failure_mode (anchoring, fixation, automation bias, deskilling, algorithm aversion)
3. ai_visibility (directive vs. compositional)
4. output_type (memo, chart, code, policy, recommendation)
5. stakes (low/medium/high)

**For the talk:** Don't show all nine cells. Select 3-4 that illustrate the governance argument most powerfully. Unpack the voxels inside each selected cell.

Suggested cells:
- **D-Read:** Coding audit data — automation bias, model pattern-recognizes confidently but misses clinical context
- **P-Think:** Retention policy gap — model interprets regulatory language softly, misses state-specific requirement
- **J-Write:** Physician documentation — model hedges on high-stakes decision, leader must own it

### Talk structure
1. Opening: "AI is already in your workflows — and it isn't asking for your prompt"
2. Two kinds of AI: directive (already there) vs. compositional (you ask it)
3. The workshop we just did Sunday — that was compositional. Why does it matter?
4. The credential argument: individual contributor vs. supervisor vs. leader
5. The 3×3 matrix — three domains, three cognitive operations, nine intersections
6. Three cells unpacked — failure modes visible in each
7. Close: "If you want to lead in HIM, you have to have felt what the model can and can't do"

### Build
- Talk outline (markdown, presenter notes)
- Slide deck (reveal.js or markdown slides consistent with existing AIX presentation stack: DM Serif Display / DM Sans, navy/crimson/gold/cream palette)
- 3×3 matrix visualization (SVG or HTML — interactive if possible, static if not)

---

## OUTPUT PATHS

Write all files to:
```
/Users/steve/Documents/aix/aix-private/projects/nyhima-workshop/
├── facilitator/
│   ├── nyhima-facilitator-deck-v2.md
│   └── talk-outline.md
├── participant/
│   ├── participant-reference-card-v2.md
│   ├── workbench-prompt.md
│   ├── round1-exercise-sheet.md
│   ├── round2-exercise-intro.md
│   ├── round3-exercise-sheet.md
│   └── round2-documents/
│       ├── R2-hipaa-minimum-necessary.md
│       ├── R2-information-blocking.md
│       ├── R2-breach-notification.md
│       ├── R2-vendor-baa.md
│       ├── R2-joint-commission-rc.md
│       ├── R2-cms-cop-medical-records.md
│       └── R2-roi-policy.md
├── resources/
│   └── system-prompts-v2.md
└── talk/
    └── talk-slides/ (reveal.js or markdown)
```

---

## MANUAL TASKS (cost to automate exceeds value — Steve does these)

- [VERIFY] Test Claude free file upload — confirm multiple files work in one conversation
- [VERIFY] Test Gemini free markdown export — confirm available, note steps
- [VERIFY] Test Gemini share link — confirm publicly accessible without login
- [DOWNLOAD] CMS Hospital General Information CSV — filter to NY, save as `NY_hospitals_2026.csv`, add to Google Drive folder
- [BUILD] Shared Google Doc template with colored participant rows
- [DISTRIBUTE] Colored cards — pick color/label system, print before June 7
- [SETUP] tiny.cc/nyhima Google Drive folder with all materials

---

## DESIGN CONSTRAINTS

- All participant-facing documents written for professionals with little to no AI literacy
- No jargon: no "LLM", no "compositional vs. directive", no "voxel"
- Tone: direct, practical, assumes professional competence
- Every exercise produces a real artifact they can use at work
- Free models only — no paid tier assumed
- Gemini free primary (data + text + charts); Claude free for Round 3 validation
- Talk uses AIX presentation stack (DM Serif Display / DM Sans / JetBrains Mono, navy/crimson/gold/cream)

---

## WHEN COMPLETE

Run `//convo nyhima-workshop` and `//goodbye` to zip outputs and close.

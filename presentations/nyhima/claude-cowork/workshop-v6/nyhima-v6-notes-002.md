---
id: v6-notes-002
type: revision-notes
parent: nyhima-facilitator-deck-v5.md
session: 2026-06-06
status: post-workshop design — Round 1 and Round 2 fully redesigned
companion: v6-notes-001.md
---

# NYHIMA v6 Notes — 002
## Session: June 6, 2026 · Round 1 and Round 2 Redesign

These notes capture the Round 1 and Round 2 redesign decisions made in the
June 6 session. Pass alongside v5.md and v6-notes-001.md to the next task.
Notes 001 covers pre-workshop fixes and tone. This file covers structural
redesign of both rounds.

---

## NOTE 1 — Round 1 data library: final decisions

**Five files selected:**

| File | CMS Dataset ID | Dataset page |
|---|---|---|
| Complications_and_Deaths-Hospital.csv | ynj2-r877 | data.cms.gov/provider-data/dataset/ynj2-r877 |
| FY_2026_Hospital_Readmissions_Reduction_Program_Hospital.csv | 9n3s-kdb3 | data.cms.gov/provider-data/dataset/9n3s-kdb3 |
| CMS_PSI_6_decimal_file.csv | muwa-iene | data.cms.gov/provider-data/dataset/muwa-iene |
| Healthcare_Associated_Infections-Hospital.csv | 77hc-ibv8 | data.cms.gov/provider-data/dataset/77hc-ibv8 |
| Maternal_Health-Hospital.csv | nrdb-3fcy | data.cms.gov/provider-data/dataset/nrdb-3fcy |

Download from the dataset page Export button. Hash-based CDN URLs change
with each CMS data refresh and are not stable links.

**Do not pre-filter to New York.**

Earlier versions of this note recommended filtering to NY before dropping
files in the folder. That recommendation is withdrawn. Give participants
the national file. "Show me only New York hospitals" is itself a Round 1
prompt — with a real failure mode (the model sometimes filters incorrectly,
misses rows, or claims to have filtered without actually doing so). Catching
that failure is a literacy lesson. Pre-filtering removes it.

**Reference document:** `cms-hospital-data-synthesis.md` exists as a
facilitator reference. It contains pre-computed NY statistics, selected
outliers, and the specific data literacy points each file surfaces. Use it
to prepare for the Round 1 debrief. Do not give it to participants.

---

## NOTE 2 — Round 1 debrief: five things the model will get wrong

From analysis of the five data files. The facilitator needs these before
the workshop. Each is a predictable model failure that participants with
HIM expertise are well-positioned to catch.

**1. ERR volatility on small N (HRRP)**
Mount Sinai West has an excess readmission ratio of 1.26 for hip/knee
replacements — on 27 cases. The model will report this as a high-readmission
hospital. A professional will ask whether 27 cases is enough to make the
ratio meaningful. It isn't. The confidence interval on 27 cases is wide.
The model will not flag this unless pushed.

**2. Missing data is not random (HAI)**
43% of NY HAI rows are "Not Available." Smaller, rural, and safety-net
hospitals are disproportionately missing — they either didn't meet reporting
thresholds, didn't submit, or were excluded for methodological reasons. The
model will analyze the 57% that reported and give a finding. It will not
tell you the finding describes only those hospitals and that the missing
43% are systematically different.

**3. PSI-90 is a composite — one PSI can drive it (PSI file)**
PSI-90 is a weighted average of 11 individual Patient Safety Indicators. A
hospital can score "Worse Than the National Value" on the composite while
having unremarkable scores on most components, because one PSI is doing
the work. The model shown a PSI-90 score will not decompose it unless asked.

**4. The denominator problem (PSI-06)**
PSI-06 (iatrogenic pneumothorax) does not adjust for procedural volume the
way mortality measures adjust for case mix. A high rate at a major academic
center performing thousands of central line insertions annually means
something different from the same rate at a community hospital. The model
will compare rates without flagging this.

**5. One answer is the finding (Maternal Health)**
SM-7 asks whether the hospital screens for maternal depression. In NY:
101 hospitals said Yes, 1 said No. The model will summarize the distribution
(66% Yes). The 1 is the story. One hospital in New York has a policy
position of not screening for maternal depression in a delivery setting.
The model will not tell you that unprompted.

---

## NOTE 3 — Round 2 complete redesign

**Old document set dumped in full:**
- hipaa-policy-manual.md (Philadelphia City HIPAA Policy Manual)
- employee-handbook-llm-ingestion.md (JHM Intrastaff Employee Handbook)
- dme-guide.md (NY Medicaid DME Guide)
- VUMC_Documentation_Standards.md (VUMC Documentation Standards)
- em-coding-guide.md (CareOregon E/M Coding Guide)

**New document set (five files):**

| Document | Source | Format |
|---|---|---|
| Model Business Associate Agreement | HHS model BAA template | PDF / convert to .md |
| Breach Notification Rule | HHS.gov | PDF / convert to .md |
| Information Blocking Exceptions | ONC/ASTP Fact Sheet, April 2024 | PDF / convert to .md |
| 42 CFR § 482.24 | eCFR, current as of June 4, 2026 | Plain text / .md |
| ICD-10-CM Guidelines (excerpt) | CMS October 2025 | PDF — **see Note 4** |

All five were uploaded June 6, 2026. Convert to .md for the Drive folder
so Gemini can read them without PDF parsing issues. The 42 CFR file is
already plain text.

---

## NOTE 4 — ICD-10-CM: must excerpt before v6 build

**[PRE-BUILD ACTION REQUIRED]**

The full October 2025 ICD-10-CM Guidelines are 100+ pages. This is not
usable in a 25-minute Round 2. Before v6 build, extract the relevant
sections and save as a standalone .md file.

**Extract these sections:**
- Section I.D — Present on Admission (POA) Reporting Guidelines
  (governs HAC and PSI-12 coding decisions; the operative section for this audience)
- Section I.C.9 — Heart failure (connects to HRRP HF measure)
- Section I.C.10 — COPD (connects to HRRP COPD measure)
- Section I.C.10 — Pneumonia (connects to HRRP pneumonia measure)

Target length: 8–15 pages. The POA section alone is worth the space —
it is the section where a coding decision either triggers or clears a PSI
flag, a HAC event, or an HRRP readmission attribution.

File to create: `icd-10-poa-and-hrrp-conditions-excerpt.md`

---

## NOTE 5 — Round 2 redesign: the prompt

The core Round 2 prompt is one sentence. It is the entire instruction.
Write it on the slide exactly like this:

> *"Here's the data story I found in Round 1. Tell me what this story
> means in the context of this document."*

This replaces the current Round 2 instruction ("paste the document, ask
it to make the thing plain, read the output like a skeptic"). That
instruction was written for long, dense documents where the model's
compression was the interpretive act. The new document set is shorter
and more structured. The task is application, not compression.

The participant brings a specific finding from Round 1. The model reads
across both the finding and the document. The participant evaluates whether
the model's interpretation is professionally adequate.

**The debrief question writes itself:**
*"What did the model explain correctly — and what did it need your
expertise to complete?"*

---

## NOTE 6 — Round 2 link map

A full data-to-document link map was produced in this session and saved as:
`r1-r2-link-map.md`

It covers all 12 data files from the broader library, not just the five
selected for the workshop. For each file it provides: the bridge question,
the primary Round 2 document pairing, a secondary option, and the judgment
hook pointing forward to the J scenarios.

**For v6 facilitator deck:** a simplified one-page version of this map
belongs in participant materials — not the full analysis, but the bridge
question for each data file. It should make Round 2 feel like a continuation
of Round 1 rather than a reset.

**The chart** (data file → document) was also produced as an inline
visualization. Reproduce it in the facilitator deck as a reference slide —
participants can use it to choose their Round 2 document based on what
they found in Round 1.

---

## NOTE 7 — Round 2 facilitator deck slides: new language

Slides 13 and 14 (Round 2 intro and how-it-works) need new language for v6.

**Current (Slide 13 — what you say):**
*"Paste the document in. Ask it to make the thing plain. Then read its
answer like a skeptic — what did it soften? what did it skip? what would
trip you up if you hadn't read the original?"*

**Replacement:**
*"Take what you found in Round 1. One finding — something that surprised
you, something you now have a question about. Choose the document that
speaks to it. Tell the model your story. Ask it what your story means in
the context of that document. Then read what comes back like a professional,
not a reader."*

**Current (Slide 14 — how it works, the code block):**
```
1. READ   Paste the document. "Put this in plain language for clinical staff."
2. THINK  Where are the traps? "What does this miss? What's legally soft?"
3. WRITE  Produce the artifact — guidance, checklist, or memo.
4. SAVE   Run the workbench prompt. Share your Gemini link in your row.
```

**Replacement:**
```
1. FIND   Take your Round 1 finding. One story. One number that surprised you.
2. CHOOSE Pick the document from the library that speaks to it.
3. TELL   "Here's what I found. What does this mean in the context of this document?"
4. EVALUATE  Read the output as a professional. Where is the model right?
             Where does it need your expertise to complete?
5. SAVE   Run the workbench prompt. Share your Gemini link in your row.
```

**Slide 15 (Round 2 debrief) — update this line:**

Current: *"A model that sounds authoritative about the law is a specific
kind of dangerous."*

Keep this — it still holds. Add after it:

*"The model applied the framework correctly and reached the wrong conclusion.
Why? That's the question. And you're the only one in this room who can
answer it."*

---

## NOTE 8 — J scenarios: forward look confirmed

The J scenarios (J1–J4) from the original workshop design remain as a
forward look, not a Round 3 replacement. The June 6 session confirmed:

- The new Round 2 documents compress the gap between Round 2 and the J
  scenarios. Participants doing Round 2 with the BAA or the Breach
  Notification Rule are doing a simplified J scenario already.
- J1 (physician who won't document) appears in the judgment hook for
  three different data files: Complications & Deaths, PSI-6, and DME.
  It is the most broadly applicable J scenario for this audience.
- J scenarios remain the "take-home" material and the Round 3 Encore C
  for fast tables. Label them in the Drive folder as: *"A harder version
  of what you did today."*
- The J scenario posture — write your position before opening the model,
  then bring it for challenge — is the LP Phase III posture. The forward
  look at the close should name this connection.

---

## OPEN ITEMS FOR V6 BUILD

- [ ] Extract ICD-10-CM POA + HRRP conditions excerpt (see Note 4)
- [ ] Convert all 5 new Round 2 documents to .md for Drive folder
- [ ] Update Slides 13, 14, 15 with new Round 2 language (see Note 7)
- [ ] Add one-page simplified link map to participant materials
- [ ] Produce the R1→R2 chart as a facilitator deck slide
- [ ] Update Slide 10 (Round 1 intro) to reflect the new data library
- [ ] Update Slide 11 (Round 1 how it works) — "any of the five files"
  not "the New York hospital file"
- [ ] Update Slide 7 (Three Moves table) — Round 2 row: *"Your expertise
  decides what the story means"* (current text: *"Your expertise decides"*
  — already close, sharpen to reflect the data story frame)
- [ ] Update workshop.html Round 2 verb card and run-of-show row to
  reflect the new document set and the data story prompt
  (see v6-notes-001.md Note 5 for the existing workshop.html update plan)

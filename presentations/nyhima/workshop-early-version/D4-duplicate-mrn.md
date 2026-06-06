---
id: D4
bucket: data
title: The Duplicate MRN Problem
tags: [patient-identity, data-integrity, MPI, duplicates]
---

## situation

Your health system recently merged with a smaller hospital. The IT team has run a preliminary analysis of the combined master patient index and flagged a duplicate record problem. You need to understand the scope and advise leadership on next steps.

## source

Master Patient Index Integrity Report — Post-Merger Analysis

Total records in combined MPI: 487,332
Potential duplicate pairs identified: 6,841
High-confidence duplicates (>90% match score): 2,104
Medium-confidence (70–89%): 3,219
Low-confidence (50–69%): 1,518

Top matching fields causing false positives:
  - Same last name + DOB, different SSN: 38%
  - Same SSN, different name spelling: 27%
  - Same name + address, different DOB: 21%
  - Other: 14%

Estimated staff hours to manually review high-confidence duplicates: 420 hours
Current MPI staff capacity: 1.5 FTE dedicated
Known patient safety incidents linked to duplicate records (prior 12 months): 3

## writing_prompt

Help me draft an executive briefing—no more than one page—that explains the duplicate record problem, why it matters for patient safety, and what we need to do about it.

## validation_prompt

I'm going to give you an AI-generated executive briefing about a patient identity integrity problem. Your job: assess whether this briefing accurately represents the urgency and complexity of the issue. What has the AI oversimplified? What would a health system executive need to know that isn't here?

## reflection

Did the AI lead with patient safety or operational burden? Which framing would actually move your leadership—and are those the same thing?

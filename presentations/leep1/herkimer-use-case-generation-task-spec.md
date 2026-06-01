---
title: County Employee AI Use Case Generation, Task Handoff
date: 2026-05-31
project: county-ai (Herkimer)
type: task handoff / specification
status: v3 (curation target set to 30 to 50; competition design opened up; em dashes removed)
runs_in: Claude Cowork
executor: any assigned task master (Paul, Alvin, Asela, Steve, Ayush). The validation protocol is a proposed baseline, a starting point these executors are free to run, vary, or replace as they compete.
companion_doc: projects/compositional-directive-framework-county-application.md (the conceptual foundation; read first)
conventions: no em dashes; prose over bullets except for the numbered production chain; grounded scenarios, not abstractions
---

# County Employee AI Use Case Generation, Task Handoff

## What this is

This document briefs the executor (a task master running the job in Claude Cowork) well enough to run it cold. The task is to generate a library of AI use cases drawn from synthetic Herkimer County job descriptions, spanning the full breadth of county roles from administrator to zookeeper. The output is content, written in markdown. Slide format is produced downstream and is out of scope.

The task serves two purposes at once. It delivers the use case content that anchors the June 10 Workshop 1 and grounds the policy arenas that follow. It also produces research data on AI human collaboration: the record of where the human validator intervened, what the model got wrong, and which judgments the model was making without surfacing them.

## The deliverable

A markdown file of 30 to 50 curated use cases. Each use case is one recognizable job moment in which a county employee encounters AI, written in the grounded register (the DSS worker photographing a client, the deputy reading a vendor risk flag, the dispatcher acting on a routing recommendation), structured consistently, and tagged on the four situational dimensions. The 30 to 50 set is a selection, not the full extraction. The chain below generates far more candidates than that, so curation is a stage with its own judgment, not an afterthought.

## The skeleton

This is the confirmed architecture. The production chain is a sequence of discrete stages. Each stage is a separate run. The human reviews the output of a stage before the next stage is triggered. The defining property of this spec is that each checkpoint names the specific judgment the human is being asked to make, not a generic instruction to review.

The stages:

1. Generate synthetic job descriptions by department and role.
2. Extract AI relevant moments from each description, by walking the five surfaces.
3. Elevate moments into use case narratives in the grounded register.
4. Tag each use case on the four dimensions.
5. Curate down to the workshop library.
6. Assemble the markdown deliverable and the run log.

## The two engines

The task runs on two distinct instruments, and keeping them distinct is the spine of the work.

The generative engine is the five surfaces. They are how the executor enumerates moments. For each role, the executor walks all five surfaces and asks at each one whether an AI moment lives there. The surfaces do generative work: they force the search into places (the embedded vendor scoring layer, the opaque data pipeline) that a thematic brainstorm would skip.

The descriptive schema is the four situational dimensions. They are how the executor tags what the surfaces surface. The dimensions describe a found moment; they do not generate it.

The two are related but not identical. The surface a moment lives on largely predicts its `ai_visibility`, but `ai_visibility` is a single ordered scale and the five surfaces are a richer generative checklist. Use the surfaces to find, the dimensions to score.

## The five surfaces (the generative engine)

1. Tool surface. AI embedded in software staff already use: Copilot in Word or Outlook, an AI feature in the case management system, dispatch software. Staff may not know it is there. Pushes embedded, often directive.

2. Prompt surface. The employee goes to a general AI tool, ChatGPT or Claude, and asks it something directly. Intentional, visible, personal. Pushes explicit and compositional.

3. Data surface. AI operating on county data in a pipeline the employee does not directly touch. Reports come out; how they were made is opaque. Pushes invisible, often directive.

4. Device surface. Personal device, personal account. The DSS photo case. County policy has no reach here unless it is explicit. Visible to the employee, ungoverned by the county.

5. Vendor surface. AI inside a procured system. The county bought a product; the model, the training data, and the scoring logic are someone else's. Embedded to invisible, and the surface where directive judgment hides best. This is the Ayush failure at county scale: a directive call the county bought without seeing.

The primary cut sits across all five. Every moment is either compositional (the employee uses AI to make something and stays upstream of consequence) or directive (the employee acts on a model's recommendation and sits downstream of the model's judgment). Directive is emphasized. Compositional cases should appear, but the directive cases are where the policy has to reach, and the easy prompt surface cases must not crowd them out.

## The production chain

Each stage names its input, the model action, the specific human judgment at the gate, what a machine verifies (so the human spends no judgment on what a check can confirm), and the output. The separation of the human judgment from the machine check is the operational form of the verification versus validation distinction: a machine confirms the work is well formed; only the human confirms the embedded judgment is right.

### Stage 1: Synthetic job descriptions

Input: the county department structure and approximate headcount (realistic low hundreds, full breadth of roles).
Model action: generate a brief functional description per role, foregrounding the data the role handles and the decisions it makes, because those are where AI attaches.
Human judgment at the gate: does each description name the role's real decisions and real data, the places where AI would actually enter? Is any high directive exposure department (DSS, Sheriff, Public Health, Probation) under weighted?
Machine check: one description per role; each names at least one decision and one data type.
Output: versioned job description set.

### Stage 2: Moment extraction across the five surfaces

Input: the job descriptions.
Model action: for each role, walk the five surfaces and extract distinct AI moments, five to ten per role, labeling each compositional or directive at the point of extraction.
Human judgment at the gate: this is the first real gate. Is each moment labeled correctly against where the judgment actually sits? A moment that looks compositional (drafting a notice) is directive if a model is scoring or routing underneath. The validator checks the label, not the prose, and pays special attention to the tool, data, and vendor surfaces where directive moments hide.
Machine check: five to ten moments per role; each carries a surface and a compositional or directive label; the set is not all compositional and not all prompt surface.
Output: versioned labeled moment list per role.

### Stage 3: Use case elevation

Input: the labeled moment list.
Model action: elevate selected moments into narratives in the grounded register. Each narrative names the role, the moment, the AI touch (where and how the model enters), and the policy question the moment raises.
Human judgment at the gate: does the narrative read as a recognizable job moment to someone who holds that job, and does it preserve the compositional or directive character rather than smoothing it into a generic AI anecdote?
Machine check: role, moment, AI touch, and policy question fields all populated.
Output: versioned use case narratives.

### Stage 4: Tagging

Input: the narratives.
Model action: tag each use case on the four dimensions (cognitive_mode, ai_visibility, output_type, stakes), then record the failure mode read and compute an attention weight as failure mode read crossed with stakes.
Human judgment at the gate: are the positions defensible, particularly `ai_visibility` on vendor and data surface cases (did the model recognize where visibility drops), and the failure mode read on the highest stakes cases? The validator spends time on the directive, invisible, irreversible cluster and lets low stakes compositional cases pass lightly.
Machine check: one value per dimension per case; failure mode read present; attention weight computed.
Output: versioned tagged library.

### Stage 5: Curation

Input: the tagged library (more candidates than the target).
Model action: select 30 to 50 for the workshop library, preserving department breadth and an adequate share of directive cases, weighting toward the high attention cluster.
Human judgment at the gate: does the selection cover the departments the workshop room will represent, and is the compositional and directive balance right, with directive adequately present? What is being dropped, and is anything dropped that the room needs to see?
Machine check: count within 30 to 50; department coverage spans the roster; directive share above a floor.
Output: versioned curated set.

### Stage 6: Assembly

Input: the curated set.
Model action: assemble the markdown deliverable, ordered or weighted by attention so the directive high stakes cluster surfaces, consistent structure per entry, plus the run log.
Human judgment at the gate: final read for coverage and balance, and confirmation the content file carries no format and no em dashes.
Machine check: count, schema validity, no missing fields, one content file plus one log file.
Output: the use case library markdown file and the run log.

## The validation protocol (proposed baseline, open)

This protocol is a baseline so the task is runnable. It is a starting point, not a constraint. The competing task masters are free to run it as written, vary it, or replace it, and to run and vary the rest of the chain as they judge best. The orchestrator chooses among the results. Whatever the mechanics, one principle should survive: the human is positioned where the model's judgment is, not where the output is.

Proposed mechanics. The two gates where judgment concentrates are Stage 2 (the compositional or directive label, checked against where the judgment sits) and Stage 4 (the tags, with care on visibility and on the high stakes failure mode reads). At these gates the validator reviews every directive case and a sample of compositional cases. The validator does not edit use cases one at a time as content. The validator answers one question per directive case: has the model correctly located where its own judgment sits, and is that the right place for the county to govern? Disagreements are logged with the validator's reasoning. That log is the research data. A machine handles everything verifiable so the human spends judgment only where judgment is required.

The open design problem for the task masters: how to surface only the directive cases for review without making the human re-read the whole library, and how to capture the validator's reasoning in a structure Asela and Ayush can process rather than free text.

## Output

File 1, content: the use case library in markdown, entries consistently structured, tagged, weighted. Content only, no format.
File 2, run log: a structured record of each stage's version, each validation decision at the judgment gates, and each logged disagreement with reasoning. This is the research artifact.

Slide format is produced downstream from File 1 and is specified separately.

## What the executor needs before starting

The county department structure and approximate headcount. The four dimension tag schema and the compositional and directive definitions as settled in the companion document. The grounded register and the document conventions. A decision on whether the vendor and data surfaces get explicit treatment in the workshop library, given that is where county exposure is largest and visibility lowest.

## Decisions on record

Curation target is 30 to 50 use cases. Competition design is left open: the task masters are not constrained to a fixed chain or a fixed validation protocol. Each is free to run and vary the production chain and the validation gates as they judge best, and the proposed baseline above is a starting point rather than a fixed structure they must hold constant.

---
title: Workshop Fully Redesigned Two Rounds Plus Talk
date: 2026-06-02
type: conversation
status: reference
project: nyhima-workshop
contributor: Steve
tags: [nyhima-workshop, ai-rtw, workshop-design, voxel-framework, talk-redesign, gemini, google-drive]
source: claude-conversation
artifacts_produced:
  - nyhima-facilitator-deck.md (needs v2 update)
  - J1-J4 revised prompts (may be repurposed for talk)
decisions_made:
  - Workshop redesigned around three rounds: Round 1 (data/Gemini), Round 2 (text/two models), Round 3 (validation with fresh model)
  - Structure: Opening (10 min) + Icebreaker (15 min) + Lightning Round guided demo (30 min) + Round 1 self-directed (30 min) + Round 2 self-directed (30 min) + Round 3 self-directed (30 min) + Wrap (15 min) = 3 hours exactly
  - Lightning round shows full arc guided by Steve, then participants repeat themselves
  - Gemini free is primary model for all rounds — handles CSV uploads, code execution, charts, native Google Docs sharing
  - ChatGPT free rejected — file upload too restricted (3/day, broken UX)
  - Round 3 validation model TBD — Claude free most likely (30MB per file, 20 files per conversation)
  - Read-Think-Write (RTW) is the cognitive spine across all three rounds
  - D-P-J scenarios map onto RTW: D=Read, P=Think, J=Write (supervisory judgment)
  - Workbench prompt is the most important prompt in the workshop — generates markdown summary of full session for Google Doc sharing
  - Google Drive infrastructure: shared folder at tiny.cc/nyhima, colored cards for participant identification, shared Google Doc template with pre-built rows, participants paste artifact links + Gemini conversation links
  - Compositional literacy (workshop) prepares HIM leaders to govern directive AI (talk argument)
  - Credential-leveled literacy framework: associate = directive user, bachelor = supervisory/compositional, master = governance/leadership
  - J scenarios (J1-J4) repurposed as directive AI use cases for the Tuesday talk
  - Talk redesigned around D-P-J × R-T-W 3x3 matrix as visible front skin of voxel framework
  - Voxel dimensions: cognitive_mode, failure_mode, ai_visibility, output_type, stakes
  - Git script drafted: simple bash alias `get "commit message"` that runs pull/add/commit/push
  - CMS Hospital General Information CSV confirmed as Round 1 dataset — filter to NY before workshop
  - Steve ran Round 1 himself using Complications_and_Deaths-State.csv on Gemini free — produced full comparative analysis of NY vs border states and national ranking, confirmed exercise works
open_questions:
  - Round 3 validation model — Claude free or other? Test file upload limits
  - Gemini native export to markdown — confirm available on free tier
  - Whether same model fresh conversation is sufficient for Round 3 validation or requires different model
  - Talk draft needs full revision to incorporate RTW framework, credential-leveled literacy argument, D-P-J × R-T-W matrix
  - Voxel framework visualization — interactive vs. static for talk slides
next_actions:
  - Build Cowork task for full workshop materials build-out (updated task generated this session)
  - Test Claude free file upload limits for Round 3
  - Test Gemini native markdown export on free tier
  - Filter CMS Hospital General Information CSV to New York
  - Revise facilitator deck to two-round + lightning round structure
  - Revise participant reference card
  - Build Round 1 exercise sheet (Gemini, CMS data, starter prompts)
  - Build Round 2 document library (7 HIM text scenarios)
  - Build workbench prompt as standalone resource
  - Build shared Google Doc template with colored participant rows
  - Revise Tuesday talk around credential-leveled literacy argument and D-P-J × R-T-W matrix
  - Write git alias script and test on non-critical repo
linked_notes:
  - conversations/steve/nyhima-workshop/2026-06-02-sprint-redesign.md
  - notes/2026-06-02-output-worth-input.md
---

Second major session on NYHIMA workshop redesign. The three-sprint structure from the morning session was further redesigned into three rounds (data, text, validation) plus a guided lightning round demo. Gemini free confirmed as primary model after Steve ran Round 1 himself using Complications_and_Deaths-State.csv — produced NY hospital comparative analysis with charts, confirmed the exercise works and is genuinely interesting. Google Drive infrastructure designed around colored participant cards, shared Google Doc template, Gemini conversation link sharing, and the workbench prompt as the key artifact-generating move. The Tuesday talk was reconceived around a credential-leveled AI literacy argument (associate/bachelor/master) with D-P-J × R-T-W as the visible front skin of the voxel taxonomy framework. J scenarios repurposed as directive AI use cases for the talk. Full Cowork build-out task updated and ready to hand off.

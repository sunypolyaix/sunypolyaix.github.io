# Morrisville Talk — Handoff for Part 2 Drafting

I'm working on a ~10-minute talk for SUNY Morrisville faculty development
(May 19, 2026). The first half is drafted. I want to draft the second half
in conversation here, then take the result back to the design tool.

## Speaker

Steven M. Schneider · SUNY Polytechnic Institute · AIX Center

## Audience

Faculty at SUNY Morrisville — a two-year applied / technical campus.
Students go into dairy, automotive tech, horticulture, ag, trades.
Not a four-year liberal-arts compositional context.

## The argument so far (first half)

The talk opens with a deliberate provocation: 100% of the content is
AI-generated (except the prompts), and the speaker will come back to that
at the end.

The core claim: most "AI literacy" pedagogy being developed right now is
built for the compositional student — sitting at a keyboard, prompting a
model, evaluating text output. That framing is wrong for Morrisville's
students. Their AI encounter is different in kind.

To make this concrete, the talk walks through three "stops":
- Dairy: robotic milking parlor + animal-level AI dashboard
- Auto shop: OBD-II scanner + AI-ranked diagnostic recommendations
- Greenhouse: autonomous irrigation, climate, disease-detection systems

In all three: the AI has already organized the field of attention before
the worker arrives. The worker's job is to maintain independent judgment
about a situation the system has already interpreted. "AI with dirty
hands." The dashboard is not the situation — it is the model's
interpretation of the situation.

The first half then introduces:
- Seven failure modes from human-factors research (manual skill atrophy,
  plan continuation bias, vigilance decrement, omission errors, commission
  errors, confirmation bias, expectation-driven processing) — all
  failures of attention.
- Three ways this round of automation is different: opaque logic, fails
  by being confidently wrong, may *increase* cognitive demand.
- A proposed design principle (not a new course): build scenarios where
  the AI recommendation is sometimes wrong by design, and students have
  to articulate why they're pausing before complying.
- Closing callback: "Can I get credit for this assignment?" is the
  four-year compositional question. It's not the most important one for
  your students. The most important question is whether they can maintain
  an independent model of the situation while AI is already organizing
  what they see.

## Current slide titles (13 slides)

01. AI literacy in applied contexts.
02. 100% of this content is AI-generated. Except my prompts.
03. Most AI literacy was built for the wrong student.
04. Stop one — The dairy farm.
05. Stop two — The auto shop.
06. Stop three — The greenhouse.
07. AI with dirty hands.
08. The dashboard is not the situation.
09. Seven failure modes, one root cause.
10. Earlier failures were mechanically legible. This round is not.
11. Design courses where students practice the moment of judgment.
12. Can I get credit for this assignment?
13. Questions & conversation.

## Full speaker notes (verbatim)

**01 · Title**
Good morning. Thanks for having me. I want to spend the next ten minutes or so talking about what AI literacy actually means for the students you teach — not the students at a four-year liberal arts school, but the students who go to work in barns and shops and greenhouses. I think the framing most institutions are using right now is wrong for your campus, and I want to make the case for a different one. Before we start, one disclosure.

**02 · Disclosure**
One hundred percent of this content is AI-generated. Everything but my prompts. I had background knowledge of Morrisville and of AI literacy before I started, but I learned the details — the aviation literature, the failure modes, the greenhouse systems — through sustained conversation with a language model. I'll come back to this at the end, because I think it actually matters for the argument. For now, let's set it aside.

**03 · Wrong student**
When most people in higher education talk about AI literacy, they mean this: a student prompts a model, gets text back, makes decisions about what to do with that output. The product is a document. The evidence of their thinking is in the conversation. That's the compositional case — and almost all of the rubrics and course guidelines being developed right now were built for it. I don't think that describes your students. So let me walk you around campus for a few minutes.

**04 · Stop one — Dairy**
Stop one. Your students working in automated dairy will encounter a milking parlor that looks something like this. Robotic systems handle the milking. The cows come and go on their own schedule. The AI monitors each animal — yield, conductivity, frequency, body weight, reproductive status. It makes feeding recommendations. It flags animals for attention. Your student's job is not to milk the cow. It's to read the dashboard, evaluate the flag, and decide whether to act on it. The system has already shaped the field of attention before your student arrives. And that word — attention — is not accidental. The architecture under many modern AI systems is literally called a transformer, built around what computer scientists call an attention mechanism: a way of weighting which signals matter most. Humans do something similar. But now another attention system is entering the workflow before the human operator begins evaluating the situation. Under what circumstances should your student override the dashboard? That is not a technical question. That is a literacy question.

**05 · Stop two — Auto shop**
Stop two. Your automotive technology students are going to work in shops where the first thing that happens when a vehicle comes in is someone plugs in an OBD-II scanner. The scanner reads the diagnostic trouble codes. AI-assisted platforms cross-reference those codes against repair records, group related codes, prioritize probable causes, and present a recommended repair sequence with confidence scores. Your student sees the recommendation on a tablet. The AI has already organized what looks important. Their attention is directed before their hands-on inspection begins. They might run additional tests. They might catch something the scanner missed. But the workflow is recommendation first, verification second — if at all. What does it take to recognize when the recommendation is wrong? That is not a scanning skill. That is a judgment skill.

**06 · Stop three — Greenhouse**
Stop three. Your horticulture students are going to manage crops in environments where AI is already making autonomous decisions. Irrigation adjusts water delivery based on soil moisture sensors and weather data — without asking anyone. Climate control sets temperature, humidity, CO2. Camera systems scan for disease and pest presence, flag anomalies, and recommend treatments. The grower — your student — receives a report. An alert. A dashboard. The system has often already acted before they see it. What does fixation look like when the disease alert fires and attention goes to the flagged plant while the actual outbreak is two rows over? What does it cost when the dashboard declares the field healthy and your student stops looking?

**07 · AI with dirty hands**
Three workers. Three dashboards. Manure on the coverall, grease under the fingernails, soil on the gloves. In each case the AI is already in the room before the worker makes a decision. Not a tool they chose to consult — a system that organized the field of attention before they looked up. This is not the compositional case. The compositional case puts a student at a keyboard, evaluating output from a model they deliberately invoked. What you are looking at is different: AI embedded in physical, high-stakes labor — recommending, flagging, acting — in workflows where the student's job is to maintain judgment about a situation the system has already interpreted. The AI got its hands dirty. That is the shift worth naming.

**08 · The dashboard is not the situation**
In all three cases the cognitive challenge is the same. The AI system increasingly organizes what the operator notices first. So the dashboard is not the situation. The dashboard is the model's interpretation of the situation. That distinction sounds small. It is the whole game. The habit of mind your students need is to maintain epistemic separation between what the model surfaced and what is actually happening in the barn, the shop, or the greenhouse.

**09 · Seven failure modes**
Human-factors researchers have documented recurring failure modes when operators work alongside automated systems. You see them in aviation, in clinical decision support, in process control. Manual skill atrophy — procedural skills degrade from disuse. Plan continuation bias — cognitive commitment to the AI-established course despite new cues. Vigilance decrement — attention drifts from primary indicators. Omission errors — failing to notice when the automation misses something. Commission errors — acting on automated recommendations without independent verification. Confirmation bias — misinterpreting ambiguous information to confirm the plan. Expectation-driven processing — seeing what the AI predicted, not what is actually there. What these have in common is not complexity. They are all failures of attention. The operator's attention has been pre-organized by the system, and independent judgment has been displaced by cue-following. Aviation addressed several of these through mandatory manual flying and scenario-based training under realistic conditions. The FAA can mandate that because the stakes are existential. Your students at Morrisville are not pilots. We do not need to train them to do everything manually as a backup. But we do need to train them to maintain an independent model of the situation.

**10 · What's different now**
Many earlier automation failures were more mechanically legible. The pump breaks. The sensor malfunctions. You can see it, you can trace it. This round is different in three ways. First, the logic is opaque. The system makes a recommendation based on patterns it learned from large amounts of data. You cannot always ask it why and get a clear answer. Second, it fails by being confidently wrong. AI can produce a plausible-looking recommendation that happens to be incorrect for your specific cow, your specific vehicle, your specific crop — and nothing in the interface signals that. Third, introducing AI into automation may actually increase the cognitive demand on the human operator. The milking robot reduced physical labor. The AI-assisted milking system requires your student to constantly evaluate recommendations from a system they cannot fully see into, at scale, every day.

**11 · What AI literacy means here**
So what does AI literacy mean here? It is not — teach students to use the tools. It is not — teach students about automation bias. It is this: design courses where students practice the moment of judgment before compliance. Where the AI recommendation is sometimes wrong by design. Where they have to articulate why they're pausing. Where following the system blindly costs them something in simulation before it costs them something in the field. Your dairy students should encounter scenarios where the feeding algorithm has miscalculated and they have to catch it by reading the herd. Your auto students should encounter vehicles where the scanner recommendation is wrong and their hands-on inspection is the only thing that catches it. Your horticulture students should encounter disease alerts that are false positives — and silent outbreaks the system missed. That is not a new course. That is a design principle you can embed in the courses you are already teaching.

**12 · Can I get credit?**
I told you I would come back to it. I said at the start that one hundred percent of this content is AI-generated, except my prompts. The full transcript of the conversations that produced this talk is in the repository I am sharing with you today. You can zip it, upload it to a language model, and ask it questions. So here is the question I want to leave with you. If a student produced this talk through sustained conversation with a model — guided it, corrected it, organized it, made the judgment calls about what to keep — can they get credit for the assignment? That is the question your colleagues at four-year compositional programs are arguing about. It is not the most important question for your students. The most important question for your students is whether they can maintain an independent model of the situation while AI is already organizing what they see. Thank you.

**13 · End / Q&A**
Happy to take questions. The repository with the full prompt transcript is linked here — feel free to grab it, run your own conversations against it, and bring the results back to your colleagues.

---

## What I want to draft now: the second half

The current draft already arcs from open → walk → pivot → diagnosis →
proposal → close. So "second half" probably means one of:

- **A deeper "what to actually do Monday morning" section** — concrete
  pedagogical moves faculty can take into their existing courses, not
  just the design principle.
- **An institutional / policy section** — what Morrisville as an
  institution should do (assessment, faculty development, employer
  conversations, accreditation framing).
- **A Q&A / objections section** — pre-empting the pushback ("we don't
  have time," "this isn't our job," "the vendors will handle it,"
  "students will figure it out").
- **Something else entirely** — e.g., a worked example of a single
  course module redesigned around the principle.

Help me decide which of these belongs in *this* talk vs. saved for a
follow-up, given the 10-minute constraint. Then help me draft titles +
speaker notes for the chosen section in the same voice and structure as
the existing slides.

## Style notes (important for matching voice)

- Conversational but tight. Speaker is a thoughtful academic, not a
  pundit.
- Short sentences. Concrete nouns. "Manure on the coverall, grease under
  the fingernails, soil on the gloves."
- Avoids AI-pitch tropes ("It's not X. It's Y." / "The magic moment" /
  faux-suspense reframes).
- Slide titles are short declarative phrases or topic noun-phrases — they
  introduce the slide, they are not the punchline.
- Repeats key phrases deliberately: "attention," "dashboard is not the
  situation," "AI with dirty hands."
- Three-beat structures (three stops, three differences, three
  scenarios). Keep the rhythm.

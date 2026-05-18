# Teaching strategies for Morrisville students

**User:** Steve  
**Created:** 5/18/2026 16:20:26  
**Updated:** 5/18/2026 16:29:40  
**Exported:** 5/18/2026 16:35:53  
**Link:** [https://claude.ai/chat/1157d0d1-b4d6-4330-9a49-ba30f8750fd3](https://claude.ai/chat/1157d0d1-b4d6-4330-9a49-ba30f8750fd3)  

## Prompt:
5/18/2026, 4:20:27 PM

> File: presentations.zip

that's kinda big? what would you do with that? could you help me understand how to teach my students at morrisville?



## Response:
5/18/2026, 4:20:50 PM

````plaintext
View: Check the skill for reading files
````

````plaintext
Bash Tool: List zip contents
````

````plaintext
Bash Tool: Read README and talk script
````

Got it. ~21MB zip, one presentation folder: `morrisville-20260519`. The core content is clear — this is your talk for tomorrow (May 19) at SUNY Morrisville Faculty Development.

**What's here:**
- `talk.txt` — full speaker script (~900 words finished, 45K word corpus behind it)
- `slides.html` + `index.html` — the actual presentation
- `drafts/` — v1–v5 evolution
- `conversations/` — source AI transcripts (dairy farming, auto tech, transformer architecture, debate)

**The argument:** Most AI literacy pedagogy was built for the compositional case (student → prompt → text). Morrisville students are *practitioners* — dairy, auto tech, greenhouse, nursing — where AI is embedded infrastructure recommending action *before* the human forms an independent assessment. The literacy challenge is maintaining an independent situational model while the AI is already organizing what you see. Seven human-factors failure modes (vigilance decrement, plan continuation bias, etc.) apply; the field hasn't built pedagogy for them.

**What I can do with this:**
- Help you workshop the talk, tighten arguments, prep for Q&A
- Extract/compare the draft versions to show evolution
- Pull the conversation transcripts to surface what research threads drove the argument
- Help you think about follow-on curriculum design for Morrisville faculty

What do you need most before tomorrow?



## Prompt:
5/18/2026, 4:21:08 PM

if i distribute that zip to folks, is it useful?



## Response:
5/18/2026, 4:21:13 PM

Probably not as-is. A zip with DS_Store files, MACOSX metadata, draft folders, and nested zips is friction for faculty who just want the talk.

What they'd actually want: the `index.html` (self-contained presentation they can open in a browser) plus maybe the README. That's it.

Options:
1. **Just share `index.html`** — drop it somewhere public (AIX repo, Google Drive link), one click to open
2. **Clean zip** — strip the cruft, include `index.html` + `README.md` + `conversations/` if you want the provenance story visible
3. **I extract and package a clean version right now**

The `make-me-public.md` file suggests you already have a publishing workflow in mind. Want me to read that first?



## Prompt:
5/18/2026, 4:21:29 PM

no, i want athem to converse with the ideas.



## Response:
5/18/2026, 4:21:35 PM

So the artifact you want isn't the slides — it's a conversational interface over the corpus.

I can build that: an AI-powered chat artifact that has the talk, the key arguments, and the Morrisville context baked into the system prompt. Faculty drop in, ask questions, push back, explore.

Want me to:
1. Extract the core corpus (talk + best draft + key conversations)
2. Build a React chat widget that calls the Anthropic API with that content as context
3. They get it as a single shareable HTML or hosted artifact

Should I pull the full `talk.txt` + `v5` draft + the dairy/auto conversations as the knowledge base?



## Prompt:
5/18/2026, 4:21:58 PM

that' s an interesting addition.



## Response:
5/18/2026, 4:22:01 PM

What's the primary thing you want them to do — interrogate the argument, explore the Morrisville-specific examples, or something else? That shapes whether the system prompt is debate-mode, socratic, or guided exploration.



## Prompt:
5/18/2026, 4:22:43 PM

i want them to do something other than listen to the talk. i want them to use the llm as guided exploration for whatevery they needs, in part inspired by the ideas discussed in the talk and in the artifact (the entire zip).



## Response:
5/18/2026, 4:24:02 PM

So the talk is a launch pad, not the content. They arrive, hear the ideas, then have a tool that helps them explore *their own* applied AI literacy questions — for their discipline, their students, their courses.

The system prompt would be something like: *you've just heard a talk about AI literacy in applied contexts; this person is a faculty member at Morrisville; help them explore what that means for their specific teaching situation* — with the corpus as background texture, not the subject.

Let me read the full corpus before building.

````plaintext
Bash Tool: Read v5 draft and make-me-public
````

Good. I have the full argument now. Let me build the tool.

The design: faculty land on it after the talk, it greets them as a Morrisville colleague, invites them to explore *their own* discipline and students — dairy, auto, horticulture, nursing, whatever. The corpus is context. The conversation goes wherever they need.

````plaintext
View: Read frontend design skill
````

````plaintext
Create File: AI-powered guided exploration tool for Morrisville faculty
````

````plaintext
Present File: /mnt/user-data/outputs/morrisville-explore.html
````

Single HTML file, self-contained. System prompt bakes in the full argument, the three stops, and the seven failure modes — but the instruction to the model is *don't summarize the talk back at them, help them think about their own discipline and courses.*

Four starter chips to break the ice: skeptics, scenario designers, people who think this is just automation bias. 

Drop it in the `morrisville-20260519/` folder alongside the slides. Or hand the URL to anyone who wants it — no zip, no friction.

> File: /mnt/user-data/outputs/morrisville-explore.html





---
Powered by [Claude Exporter](https://www.ai-chat-exporter.net)
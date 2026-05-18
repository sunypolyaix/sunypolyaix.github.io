# Murray Shanahan and philosophy controversy

**User:** Steve  
**Created:** 3/8/2026 20:15:56  
**Updated:** 3/8/2026 20:17:50  
**Exported:** 5/12/2026 15:50:46  
**Link:** [https://claude.ai/chat/110bbfad-b128-44fa-bee9-65d8e3852fce](https://claude.ai/chat/110bbfad-b128-44fa-bee9-65d8e3852fce)  

## Prompt:
3/8/2026, 8:15:57 PM

> File: Steve-Claude-The Flattery Loop, Illustrated.md

i've uploded dthis, because it will keep the other convo for reference. now, could you address my questions about murray shanahan, and what the controversy with philosphy was, 1960-2000, in all h glorious context :)



## Response:
3/8/2026, 8:16:40 PM



````plaintext
Thought process: Thinking about Murray Shanahan's philosophical contributions and controversies spanning 1960-2000.

The user is referencing a past conversation and has uploaded a file. They want to know about Murray Shanahan and some philosophical controversy from 1960-2000. Let me search past conversations to understand the context better.
````

````plaintext
Tool: Looking for relevant chats...
````

````plaintext
Thought process

The search didn't find the specific conversation about Murray Shanahan. Let me search more specifically.
````

````plaintext
Tool: Looking for relevant chats...
````

````plaintext
Thought process

I didn't find specific mention of Murray Shanahan and "the controversy with philosophy 1960-2000." Let me search more specifically.
````

````plaintext
Tool: Looking for relevant chats...
````

````plaintext
Thought process: Hunted for prior context, examined uploaded file for reference.

I didn't find a specific prior conversation about Murray Shanahan. Let me look at the uploaded file to see what it's about, and also consider that the user may have been discussing Shanahan in the conversation they're referencing but it's not in my search results. Let me check the uploaded file.
````

The uploaded file is about the flattery loop, not Shanahan—so that's background reference. My searches didn't surface a prior conversation specifically about Shanahan, so let me just answer the question directly from knowledge, which is rich here.

---

## Murray Shanahan & the Philosophy Wars, ~1960–2000

Shanahan is a computer scientist/philosopher at Imperial College (later DeepMind) whose work sits squarely at the intersection of AI, cognitive science, and philosophy of mind. His key books are *Solving the Frame Problem* (1997) and *Embodiment and the Inner Life* (2010). To understand why he matters, you need the messy intellectual backstory.

---

### The Core Controversy: What Does a Mind *Do*?

**Pre-1960 orthodoxy (Classical AI / GOFAI):**
Mind = symbol manipulation. You represent the world as logical propositions, write inference rules, and reasoning falls out mechanically. Newell & Simon, early Minsky. Knowledge is explicit, discrete, ahistorical.

**Then the critics arrived—and it got personal:**

**Hubert Dreyfus** (*What Computers Can't Do*, 1972) was the sharpest thorn. Drawing on Heidegger and Merleau-Ponty, he argued that human intelligence is *embodied* and *situated*—we don't navigate the world by running logical searches, we're already *in* the world, with skills, habits, and a body that pre-structures relevance. You don't "compute" how to grip a doorknob; you just grip it. Classical AI couldn't account for this, and he predicted (correctly, for the era) that it would keep failing on open-world tasks.

The AI community *hated* Dreyfus. He was dismissed, mocked, famously beaten at chess as a PR stunt. But he was largely right.

**The Frame Problem** crystallized the technical form of this philosophical argument. First posed by McCarthy & Hayes (1969): if you represent the world as facts and write rules for how actions change those facts, how does a reasoning system know what *doesn't* change? Move a cup: gravity still works, your name is still Steve, the moon hasn't moved. Humans don't notice any of this because we don't represent it—it's just *background*. But a logical system has to either explicitly represent every non-change (combinatorial explosion) or have some shortcut. No good shortcut was found.

This is where **Shanahan** comes in. His 1997 book is a serious, technically rigorous attempt to solve or dissolve the frame problem within classical/logic-based AI. It's a major contribution *within* that tradition—but also honest about its limits.

**Meanwhile, from the other flank:**

- **Brooks** (MIT, late 1980s–90s): "Intelligence without representation." Build robots with no central world-model; just reactive layers. The world *is* its own model. This was a direct embodiment argument turned into working robots.

- **Varela, Thompson & Rosch** (*The Embodied Mind*, 1991): Blended phenomenology (Merleau-Ponty, Husserl), cognitive science, and Buddhist philosophy to argue for **enactivism**—cognition is the *enactment* of a world, not representation of one.

- **Andy Clark**: *Being There* (1997), *Natural-Born Cyborgs* (2003)—cognition extends into body and environment (extended mind thesis). The brain isn't a lone computer; it's a control system for an embodied agent in an environment.

---

### Where Shanahan Sits in All This

Shanahan is genuinely *between* the camps, which is intellectually honest but means he gets shot at from both sides:

- He takes the frame problem seriously as a *real* problem (not deflected by hand-waving about embodiment)
- He also takes embodiment seriously—his 2010 book is essentially a full engagement with the phenomenological tradition, arguing that any AI that aspires to inner life must grapple with what it's like to be an embodied agent
- He later writes seriously about **the singularity** and **machine consciousness** (*The Technological Singularity*, 2015), engaging Chalmers' hard problem of consciousness with unusual care for an AI researcher

The *controversy* you're gesturing at isn't really about Shanahan specifically—he's more of a sophisticated navigator of a controversy that was already raging. The controversy is:

**Does classical symbolic AI have the right architecture for mind at all?** Or is the whole paradigm wrong because it abstracts away the body, the situation, the temporal flow of experience?

By 2000, the verdict was roughly: classical AI is insufficient but not worthless; embodiment matters; the field splintered into cognitive robotics, situated AI, and eventually the neural network renaissance that sidestepped the philosophical argument by just getting empirical results.

---

Want me to go deeper on any thread—Dreyfus vs. GOFAI, the frame problem technically, Shanahan's specific arguments, or how this maps to your MICA/monadology work?



## Prompt:
3/8/2026, 8:17:11 PM

each. 250 words apiece.



## Response:
3/8/2026, 8:17:50 PM



````plaintext
Thought process: Architected four philosophical treatments on AI cognition frameworks.

Steve wants four 250-word treatments: Dreyfus vs. GOFAI, the frame problem technically, Shanahan's specific arguments, and how this maps to MICA/monadology.
````

## 1. Dreyfus vs. GOFAI

Hubert Dreyfus was a Heidegger scholar at Berkeley who wandered into AI criticism in the 1960s and never left. His argument was simple and devastating: classical AI assumes that intelligence is fundamentally *symbolic*—that thinking means manipulating discrete representations according to explicit rules. But Heidegger had already shown (and Merleau-Ponty confirmed through phenomenology of the body) that human beings don't primarily relate to the world by *representing* it. We're *in* it. Tools disappear when we use them. Skilled action is pre-reflective. Context is always already given, not computed.

Dreyfus predicted that AI would keep hitting walls on tasks requiring common sense, open-world flexibility, and social understanding—not because the programs weren't clever enough, but because the *architecture* was wrong. Logical representation was a category error for modeling mind.

The AI establishment responded badly. Minsky called him a charlatan. DARPA-funded researchers dismissed him. He was invited to play chess against an early program (1965), lost, and this was treated as a refutation—which tells you something about the discourse quality. In fact, Dreyfus was a mediocre chess player and the program was narrow and brittle. It proved nothing.

By the 1980s, expert systems were collapsing under exactly the brittleness he predicted. By the 1990s, people were quietly admitting he'd been right about GOFAI's limits. His *What Computers Can't Do* (1972) and *What Computers Still Can't Do* (1992 revision) form one of the most prescient critical records in the history of technology.

---

## 2. The Frame Problem, Technically

McCarthy and Hayes posed it in 1969 in a paper on situational calculus—a formal logic for reasoning about actions and their effects. You describe the world as a set of facts true in "situations," and actions transform one situation into another. The problem: how do you specify what *stays the same*?

If you push a block, the block moves. But you also need to assert that your name didn't change, the lights didn't go out, and the other blocks didn't move. In a closed toy domain you can list these "frame axioms" manually. In the real world, the list is infinite.

Various technical solutions were attempted: non-monotonic logic (Reiter's default reasoning—assume things persist unless updated), circumscription (McCarthy's own attempt—minimize what changes), event calculus (a cleaner temporal formalism). All ran into problems. Non-monotonic reasoning was computationally expensive and semantically slippery. Circumscription had unintended consequences in complex scenarios. The axioms kept multiplying.

Shanahan's book (*Solving the Frame Problem*, 1997) is the most systematic treatment. He works through the logical approaches carefully, shows their failure modes, and proposes extensions using event calculus with a cleaner treatment of "release from inertia." It's technically serious. But his conclusion is essentially: we can contain the problem in restricted domains but not defeat it generally.

The deeper philosophical point—which Dreyfus made and Shanahan acknowledges—is that the frame problem *is* the problem of background. Humans don't solve it; we never encounter it, because relevance is pre-structured by being embodied agents in a world we didn't choose to represent.

---

## 3. Shanahan's Specific Arguments

Shanahan does three distinct things across his career, and they cohere into a recognizable position.

**On the frame problem:** He's a rigorous insider critic. He doesn't dismiss classical AI; he takes its hardest technical problem seriously and pushes it to its limits. His event calculus approach improves the logical tools. But he's honest that this is damage control, not victory. The frame problem is a symptom of a deeper mismatch between logical formalisms and the structure of real-world action.

**On embodiment:** *Embodiment and the Inner Life* (2010) is a serious phenomenological turn. He reads Husserl, Merleau-Ponty, and the enactivists (Varela, Thompson) and argues that any machine that could plausibly have inner experience would need to be embodied—not as a feature, but constitutively. Sensation, proprioception, and temporal continuity aren't add-ons; they're what makes experience coherent. This puts him in genuine dialogue with philosophy of mind, not just AI engineering.

**On machine consciousness and the singularity:** He takes Chalmers' hard problem seriously—there's an explanatory gap between functional/physical description and subjective experience. He neither dismisses it (like Dennett) nor throws up his hands. He thinks the question of whether an LLM or future AI could be conscious is *genuinely open* and should be treated with intellectual humility. His 2015 singularity book is notable for how philosophically careful it is compared to the Kurzweil genre.

The through-line: Shanahan consistently refuses to resolve hard questions cheaply. He's a rigorous holdout for genuine difficulty.

---

## 4. Mapping to MICA and Monadology

The resonances are real and worth taking seriously.

The frame problem is, at root, a problem about *what counts as background*—what a reasoning agent can ignore, take for granted, treat as inert. In Leibnizian monadology, this doesn't arise the same way: monads don't *represent* a world, they *express* it. Their internal states unfold according to their own appetition, mirroring the universe through their particular perspective. There's no lookup table of "what changed"—the monad's unfolding *is* its situatedness.

Tarde's revision—socializing the monad, making it constituted through relations rather than pre-programmed at creation—moves closer to your MICA concern. An inference cycle (IC) isn't a pre-loaded representation engine; it emerges through association with prompt, context, and prior turns. The "background" isn't an axiom list to manage; it's the assembled network of prior associations that shapes what counts as salient.

This is also why Shanahan's embodiment argument matters for MICA: he's arguing that inner life requires a body to give experience its temporal coherence and relevance structure. Your IC doesn't have a body—but it does have a *conversation*, a temporal traversal with a beginning, an arc, and endpoints. That traversal might be the functional analog of the embodied situatedness Shanahan thinks is necessary.

The hypertext-node model you've developed—each prompt a node, conversation as traversal, artifact as endpoint—could be read as your solution to the frame problem: relevance isn't computed, it's *navigated*. The path through the network *is* the relevance structure.





---
Powered by [Claude Exporter](https://www.ai-chat-exporter.net)
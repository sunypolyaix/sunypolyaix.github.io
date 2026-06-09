# Reading and Writing with AI: How We Live with a New Kind of Mind — v3

*NYHIMA Annual Conference · Breakout Session · Emerging Trends · Tuesday, June 9, 2026 · Turning Stone Resort, Verona, NY*

*Update notes: collaborative tone throughout; expert-distance language removed; cost section reframed; electronics and digital sentences added to timeline; model-in-the-loop close.*

---

## 1 · The longest story we are part of

I want to start a long way back. Further back than computers, much further back than this technology, because I don't think you can see what's actually happening right now until you see the line it sits on. And the line turns out to be very long.

Here's the thing I keep coming back to. For as long as there have been people, we've had one stubborn problem: a thought lives in one head, and it dies there, unless we can get it out. And so the whole history of our species, in a way, is the history of getting thought out of the head — finding ways to hold it, move it, work on it, hand it to someone who wasn't in the room. Once you start looking at it that way, the whole sweep of it lines up.

Start with spoken language. Somewhere deep in prehistory — tens of thousands of years ago — we develop symbolic speech. Words that hold steady. Words that mean the same thing tomorrow as they do today, that a person who wasn't there can still understand. And suddenly a thought can travel — voice, to ear, to another mind. That's the first container thought ever lived in. And for most of human history, it's the only one. Your knowledge lived in you, and in the people close enough to hear you, and nowhere else.

Then look what happens. About ten thousand years ago, clay tokens. People press shapes into clay to keep track of things — so many sheep, so many measures of grain. It sounds almost too small to mention. But look at what it actually is: for the first time, a piece of human thinking lives *outside* a human being. In matter. Where it doesn't depend on anyone remembering it. Many scholars think this is the seed writing grows from. A thought, set down in the world.

Then writing itself, around five thousand years ago — in Mesopotamia, in Egypt, more or less independently. And now it's not just counts. Now it's language. Thought moves from voice and ear to hand and eye. What used to live only in the air, in the moment of speaking, can be set down and still be there when the speaker is gone.

Then the alphabet, roughly thirty-five hundred years ago. A small set of reusable pieces — letters — and out of them, anything. Now, other great writing systems did fine without one; this isn't the only road. But the alphabet made writing easier to learn and easier to spread. You don't need thousands of symbols anymore. You need a couple dozen, and the knack of putting them together.

And then, much later — about five hundred and eighty years ago — Gutenberg. The printing press. And the press does for *copies* what the alphabet did for *composing*: it breaks text into pieces you can set and reset and reuse, and it makes any text, in any number, anywhere. Thought that used to be rare and expensive and locked away comes pouring out into whole populations.

Then, in the nineteenth and twentieth centuries, electronics — telegraph, telephone, radio, television — and the speed of thought jumps again, until what once took weeks to cross a continent moves at the speed of light.

Then digital, and computing breaks language down into smaller and smaller pieces — characters into bits, bits into the smallest things we can store — so we can find them faster and faster, sort them, and string them back together, but only ever rearranging what we already made, never regenerating it.

Now here's what I want you to notice — because once you see it, you can't unsee it. Look at what every one of those steps has in common. Every single one is a human being, taking human thought, and putting it into the world so it can be kept and shared. Tokens, writing, alphabet, print — each one reaches a little further than the last. But in every case, from the clay token to the printed book, the human is the one making the thought. The technology carries it. Multiplies it. Holds it. It never makes it. We make it. And that holds for ten thousand years.

Now — there's a version of this story that's too clean, so let me complicate it. People had been teaching machines to produce language for decades before any of us noticed. Back in the nineteen-sixties, a program called ELIZA could hold a kind of conversation. There were translation systems. The technology that would become ChatGPT was generating text in labs for years before we saw it. So a machine didn't make its first sentence in 2022.

What I am going to tell you is this. For ten thousand years, the making stayed ours — in practice, in daily life, the creating was something humans did, and the machines, however clever, carried what we made.

And then that walks out of the lab, and into every hand on Earth, on November 30th, 2022.

---

## 2 · The break

On November 30th, 2022, a system called ChatGPT goes public — and all at once, anyone can sit down at a machine, ask it almost anything, at any hour, and watch it produce language back. Not look it up. Not play back something a person wrote. Produce it. Open-ended language, about anything you ask, made on the spot.

And I want to be careful to say what's new here, because it's easy to overshoot. A calculator produces a number — but you chose the operation. A search engine ranks pages that already exist. This is a different thing. You put a question to it, in plain language, on any subject you like, and it writes you something that wasn't there before. That's the part no earlier augmentation could do. And within five days, a million people were doing it.

Now, that first version — by today's standards, it wasn't much. It got things wrong. It made things up. It wouldn't have fooled you for long. And none of that is the point. The point isn't that it was good. The point is what it *did*: it composed. The augmentations before it carried our thought. This one writes its own. Clumsily at first. Much better now. But it writes. That's not a faster tool. That's a different kind of thing.

And I find the most useful way to hold that — the framing that's helped me most — comes from Geoffrey Hinton, one of the people most responsible for this technology even existing. He's argued that we might be looking at a genuinely different *form* of intelligence. Not a copy of ours. Not a simulation of a human mind. Something else. Now, I'm not telling you that's a settled fact — nobody can tell you that yet, and people who know far more than I do are arguing about it right now. But I'll tell you why I find the framing useful: it keeps me from the two easy mistakes. It is not a person. And it is not a calculator with a vocabulary. It's a new kind of thing, and we don't have good instincts for it yet, because we've never had one before.

That's where we actually are. Ten thousand years of carrying human thought — and now, suddenly, something that doesn't just carry it but produces it. And we're the first people who've ever had to live alongside that. Not look back on it from a safe distance. Live in it, while it's happening, before anyone has it figured out.

So the rest of what I want to do with you is think about how we do that.

---

## 3 · What the thing actually is

Before we can talk about how to live with something, we should probably know what it is. And the good news is it's a lot less mysterious than it looks — a fair amount of the mystery is manufactured, and I don't think it serves any of us.

So let me get specific. We keep saying "AI." What we're really talking about is a Large Language Model — an LLM — and the systems you've heard of are built on it. ChatGPT. Claude. Gemini. Copilot, which is probably the one that turned up in your software at work. Perplexity. Different companies; the same kind of thing underneath.

And here's how it comes to be. You take an enormous amount of written text — a huge slice of everything humanity has digitized and put within reach. Not all of it. Not close to all of it — and that matters, because whatever gets left out, stays out. But a vast amount. And the system works through all of it and builds something like a giant map of relationships: how words follow words, how ideas sit near other ideas, how concepts connect. It isn't filing the documents away to look them up later — though, interestingly, it learns some passages well enough to reproduce them, which is its own thorny issue. Mostly it's learning the *patterns*. And from that map of patterns, it produces new text that fits. You ask it what fear is, what the French Revolution was about, how to phrase a hard paragraph — and it builds you an answer by predicting, piece by piece, what should plausibly come next.

That's worth sitting with for a second, because it explains both what these things are wonderful at and where they fall down. They're pattern-completion machines of staggering range. They'll speak fluently on almost anything you put to them. The newer ones will sometimes tell you they're unsure — but understand, the whole machine is built to *produce a response*, not to sit there in silence. Producing is what it does best. Which means it can be completely fluent and completely wrong in exactly the same voice. The confidence isn't a signal that it's right. It's just how it talks.

And here's one more piece that changes how I think about the whole thing. The model isn't awake. It isn't sitting there thinking about you while you're away. It's dormant. You send it a question; it wakes up, generates a response, and goes back to sleep. Question in, generation out, then nothing. That single round-trip is the whole event. There's no continuous mind on the other side, watching, waiting. There's a system that switches on when you ask, and is otherwise still.

This is why I keep saying it isn't your grandfather's AI. If you're twenty-five, your grandfather's AI was the expert system. Some of those were genuinely powerful inside a narrow lane — but they ran on rules people wrote out by hand. *If this, then that.* Ask one something outside its rules, and it had nothing for you. It could only give back what someone had already put in. This is the opposite. You can ask one of these models a question nobody ever anticipated, and it'll build you *something* — coherent, plausible, sometimes wrong, but made fresh. The old machine looked things up. This one composes. And that's the whole difference — the difference that landed in everyone's hands in 2022.

---

## 4 · What it costs, and what we don't know

There's a part of this I find genuinely hard to hold in my head, because it's so at odds with how the thing feels to use. The screen is so clean. The answer just appears. And underneath that clean surface is one of the heaviest physical objects we've ever made.

Kate Crawford has traced this more carefully than most, and what she follows is the whole physical body of it. The electricity — these models run in data centers, buildings full of specialized machines, going up right now at a pace that rivals almost anything in the history of construction. The water that cools them. And the minerals the hardware is made of: lithium, cobalt, rare earth elements, pulled out of the ground in particular places, at real human and environmental cost. The chip in the clean machine starts in a mine. And the systems learned to be this smooth in part through human labor — people, a lot of them low-paid, a lot of them in the Global South, doing the work of labeling and filtering the worst of the training data so the rest of us never see it. So the seamlessness is built on something, and the something isn't seamless. The exact figures get argued about — anyone who hands you one clean number is overselling it — but the direction doesn't: this is one of the more physically demanding things we've ever built, and it's growing fast. There's no free question. Every one of them draws on the world somewhere.

And there's a real intellectual question sitting underneath all of this — one I don't think any of us should be too quick to settle. There's a well-known critique, the "stochastic parrots" argument, that says these systems don't understand anything at all. That they're just very sophisticated pattern-matchers, stitching together plausible runs of words with nothing underneath, and that we're fooling ourselves when we treat the fluent output as thought. And I think there's a lot to it. I also think it's genuinely open. Whether what these systems do turns out to be a new kind of thinking, or only a very convincing imitation of one — that's the kind of question this profession, and this whole culture, gets to actually argue about. We don't have to inherit the answer. We get to work it out.

So the cost is real, and the doubt is real, and I want to keep both of them in view. And even with both of them in view, here's where I come down — and why I don't think the answer is to back away.

---

## 5 · The turn

Here's the thing I most want to share with you, because it's the thing that changed how I see all of this.

Go back to that long line we walked at the start — tokens, writing, the alphabet, the press. Every one of those was an augmentation. A way of reaching past the limits of a single head. And here's what's easy to forget: every one of them, when it showed up, frightened people. The oldest example we have is Plato — writing about *writing itself*, twenty-four hundred years ago. He worried it would weaken memory, that it would give people the *appearance* of wisdom in place of the real thing. And he wasn't entirely wrong! Something did change. But look what happened. We took up writing anyway, and memory changed, and we did not lose our minds. We got science. We got law. We got medicine, and records, and this conference. The augmentation didn't hollow us out. It enlarged us. It made us capable of things we couldn't have reached without it.

Now, let me be careful here, because there's a sloppy version of this that's just false. I am *not* telling you every fear about every technology has been wrong. Plenty were right. Nuclear weapons earned their fear. So did leaded gasoline. So did the surveillance machine, and some of what the last twenty years of screens have done to us. Technology can wound, and pretending otherwise is its own kind of foolishness. But there's one *particular* fear with a remarkably bad track record — and it's a specific one. It's the fear that a new tool for *thinking* will hollow out the human mind. That the written word will rot our memory. That print will drown judgment in cheap opinion. That the calculator will kill arithmetic. That *this* — whatever the current "this" happens to be — will make us less.

That fear is ancient. It comes back with every single augmentation of thought. And so far, every time, the augmentation has *enlarged* what a human being can do, not shrunk it.

And that's the fear in this room right now, about AI. I can feel it; I think you can too. And what I want to offer is just this: weigh it against a very long losing streak.

Because — and here's where it gets genuinely new — I'm not going to promise you this time is exactly like the others. This time really is different. This is the first augmentation that generates open-ended language, on any subject, in the hands of ordinary people. That's new. New things deserve real caution — that's exactly why I put the costs and the doubts on the table a minute ago. But the difference cuts *both ways.* The very thing that makes this unsettling — that it generates, that it might be a different kind of mind altogether — is the same thing that makes it more than any augmentation we've ever had.

Think about it. A tool that only carries thought is a tool. But a thing that *generates* — that you can ask, that answers, that works a problem right alongside you — that's not just a tool anymore. It's something closer to an assistant. A collaborator. And here's where it gets strange, and I'd rather name the strangeness than smooth it over: some people find themselves treating it as a companion. I told you a minute ago it isn't a person, and I meant it — it isn't. And yet people talk to it like a *someone*, and feel met by it, and that isn't simply a mistake on their part, because the thing genuinely answers. A not-person that we relate to as a someone. We've never had that before. We don't even have a word for it. And the gap between what it *is* and how it *feels to use* is one of the central things we're going to have to learn to live inside. It is — to borrow the idea I keep returning to — a genuinely exotic kind of mind. Not human. Not pretending to be human. But able to do something no augmentation ever could: meet us in language, and generate.

So here's the posture I've landed on. Not defense. Not backing away. Not pretending it isn't here — and not handing ourselves over to it completely, either. The threat is real. But a threat is a *condition* — something you engage, with your eyes open — not a verdict you flee from. And engaging it with your eyes open is the whole of what I mean by agency. The people who came through every earlier one of these shifts intact weren't the ones who refused the new thing, and they weren't the ones who let it run them. They were the ones who picked it up on purpose, learned what it actually was, and decided — for themselves — how they'd use it. That choice is sitting right in front of you. It's really the only thing being asked of you.

---

## 6 · How I live with it

So let me end by just showing you how I actually live with this. Not a prescription — I'm not going to tell you to do it my way. Just a glimpse of what it looks like from inside one person's days.

Here's the first thing worth saying plainly: we built these things. This new kind of mind didn't arrive from somewhere else. We made it, out of our own written record, with our own hands and a staggering amount of our own resources. It's here because we chose to build it. Which means the question of what we do with it was never really a question about the technology. It's a question about us. Ted Nelson saw this a long time ago — decades before any of it was possible, he imagined machines that would augment human thought, documents you could think *with*. He had a line for what he was after: *making people freer through computers.* That was the dream. And in a strange, partial, complicated way, it's arrived. We have, now, a thing we can genuinely think alongside. The dream came true — and, like most dreams that come true, it came true sideways, with costs and doubts attached. That doesn't make it less of an arrival.

So here's what it looks like for me. I'm aiming for a place — I'm mostly there already — where I open my laptop in the morning and I say, *hello, Claude* — my model of the week — or just, *hello, language model. What's on the agenda today?* And my work starts in the model, and it very nearly ends there too. I don't really open a word processor anymore. I don't open a spreadsheet. The work happens in conversation with this thing.

And I've started every task, for a while now, with one question: *how can I use AI to do this?* I call it keeping the model in the loop. You've probably heard "human in the loop" — the human kept in the chain to check the machine. I mean something closer to the reverse. I'm still doing my work. The same work I've always done — the reading, the thinking, the deciding what's worth saying. But wherever I can, I put the model into the loop. Not to do the thinking for me. To think *with*. To draft what I'll revise, to bring me more than I could have gathered alone, to argue with, to push against, while the judgment about what matters stays mine.

That's the whole of it, really. That's what living with AI looks like from where I stand. Not a tool I pick up and put down. A new kind of mind I've folded into the loop of my own thinking — and I'm more capable for it, not less.

And that's what I'd leave you with. Not a worry. Not a warning. An invitation — the same one every generation got when its great augmentation arrived, and answered well. Pick it up. Pay attention. Decide for yourself how you'll think with it, read with it, write with it.

That's what it means to live with AI.

Thank you.

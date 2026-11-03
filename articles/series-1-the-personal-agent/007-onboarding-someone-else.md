---
entry: 7
title: "Onboarding Someone Else"
series: 1
series_title: "The Personal Agent"
date: 2026-11-03
status: Living
patterns: [1, 4, 5]
terms: [personal-agent, personal-context-os, coding-agent, skill, context, commit]
---

# Article 007 — Onboarding Someone Else

## The story

- **The setup worked for one person.** By late October 2026 my own system —
  a Personal Context OS, a personal agent that loads it, one room per
  project — was running my weeks (Article 001). The obvious next question:
  does any of it transfer, or is it fitted so tightly to me that it only
  works here?
- **The first student.** The lead pastor at my church — we meet every Monday
  morning — was the natural test. Earlier I had helped him start a Personal
  Context OS of his own: his identity, his preferences, his work, written
  down in files he owns, in his own words.
- **He took it from there.** He spent time answering his AI's questions and
  improving the files, then had the AI save the updates back to his
  repository — approving each commit himself before it landed.
- **November 2, 2026.** I helped him onboard a personal agent of his own.
  He named it after his dog and set the dog's photo as its avatar — the same
  small move I made when I named mine after my cat. It sounds like a detail;
  it is not. An agent with a name and a face stops being a tool you visit
  and starts being a colleague you work with.
- **The instructions I left him.** Six steps, written for a beginner, in the
  order that makes them work:
  1. Once you have answered enough of the AI's questions, ask it to update
     your Personal Context OS on GitHub. It may ask permission to commit
     changes and push to main — that approval is yours to give, each time.
  2. Ask your agent to load the updated Personal Context OS, so it can work
     better for you — from your current truth, not from its memory of an old
     conversation.
  3. Set up a coding agent on your computer together with your agent: go
     through the login, choose a default model, and set a token usage limit.
     Ask the agent to guide you through the setup; you do not need to
     already know how.
  4. Show your agent one real job you already do every week — his was making
     short video clips from sermon recordings — and have it record the job
     as a **skill**, so it can do the job for you in the future, the same
     way every time.
  5. You can even link the entire workflow: capturing the video, matching
     the audio, clipping it with the coding agent, human review — of
     course — and uploading to YouTube.
  6. One automation at a time. Be creative and have fun!
- **What I noticed.** Nothing in the six steps is about me. The order is the
  whole secret: context first, because an agent that does not know you can
  only guess; the agent second, because it is the one who loads the context;
  the power tools third, with limits set while a human is watching; and one
  real workflow last, because a skill taught on real work is worth ten
  demos. Teaching the system took an afternoon. Building it the first time
  took a season.

## In plain words

- **Personal agent** — an AI agent set up for one person: it knows your
  work, your preferences, and your projects, and acts as your assistant.
- **Personal Context OS** — a private repository of curated Markdown files —
  identity, preferences, domains, projects — that any assistant can load, so
  the agent starts from what you wrote down, not from a blank slate.
- **Coding agent** — an AI agent that works on your own computer through a
  command line: reading and editing files, running tools, doing the
  mechanical parts of a job while you direct it. Claude Code and Codex are
  the two I have used.
- **Skill** — a reusable, step-by-step capability packaged as files: it
  teaches an agent how to do one job well, the same way every time.
- **Context** — everything the agent knows about you and your work at the
  moment it acts. When the context lives in files that are kept updated,
  every tool the person uses shares the same truth.
- **Commit** — one saved change to a repository, with a note saying what
  changed. Approving the commit is how the owner stays the owner.

Every term also lives in the [glossary](../../glossary.md).

## How it works

The transfer works because the layers are separate (Pattern 2), so each one
can be handed over on its own:

```text
The person — every irreversible decision stays theirs
│
├── 1. Their Context OS — their words, their files, their repository
├── 2. Their personal agent — loads the Context OS, knows the person
├── 3. Their coding agent — set up together, with a model and a limit
└── 4. Their first skill — one real weekly job, taught end to end,
       with human review before anything is published
```

My role shrank as the afternoon went on: I explained the first layer, sat
beside him for the second, mostly watched the third, and only advised on
the fourth. That shrinking is the goal. A system only one person can
operate is a hobby; a system a second person can pick up in an afternoon
is a playbook.

## Try it yourself

Onboarding someone else, the smallest version:

1. **Start from their work, not your setup.** Ask what their week actually
   contains and what they already repeat by hand. Their Context OS has to
   describe their life, or the agent will faithfully serve a stranger.
2. **Let them answer in their own words.** Resist editing their context
   into your voice. The files work because the person recognizes themselves
   in them.
3. **Keep every approval with them.** Their commits, their accounts, their
   uploads. You are teaching, not taking over — the moment you hold their
   keys, you have built them a dependency, not a system.
4. **Teach one workflow they already do weekly**, and have the agent record
   it as a skill while you both watch. One. The second automation is next
   week's lesson.
5. **Leave them a short list, not a manual.** Six steps fit on an index
   card. If the handover needs a binder, the system is too complex — for
   them, and probably for you.

## What it proved

Three patterns from [patterns.md](../../patterns.md), holding up on a
second person:

- **Pattern 1 — Context is infrastructure you own.** His setup survived
  the transfer because the context was files, not conversation history
  inside one app — portable to his agent, his coding tool, his next model.
- **Pattern 4 — The human keeps the irreversible decisions.** Every gate in
  the six steps — the commit approval, the login, the token limit, the
  review before upload — stays with the person. The agents do the work; he
  keeps the keys.
- **Pattern 5 — Minimum viable complexity.** One automation at a time is
  not caution; it is the pace at which a beginner actually absorbs a
  system. Six steps, one afternoon, no binder.

And one thing that is not a pattern yet, only an observation: the
playbook's compound interest is other people. Every person onboarded this
way becomes someone who can onboard the next.

---

*Articles 002–006 remain planned. This entry was written out of order, in
the week the experience happened, because the journey does not always wait
for the outline.*

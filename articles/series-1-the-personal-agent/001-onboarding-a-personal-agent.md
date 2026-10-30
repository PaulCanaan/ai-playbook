---
entry: 1
title: "Onboarding a Personal Agent"
series: 1
series_title: "The Personal Agent"
date: 2026-10-30
status: Living
patterns: [1, 2, 3, 4, 5, 6]
terms: [ai-agent, personal-agent, github, repository, commit, context, side-chat, orchestrator]
---

# Article 001 — Onboarding a Personal Agent

## The story

- **Late September 2026.** I onboarded a personal AI agent (Muse; my
  assistant runs as "Baby Fish") and began delegating real work: email,
  scheduling, research, monitoring, writing and ministry projects.
- **The bottleneck.** An agent without durable context restarts from zero.
  Re-explaining identity, preferences, and project state every session does
  not scale, and the agent's guesses fill the gaps badly.
- **Mid-October 2026.** I built the **Personal Context OS**: a private
  repository of curated Markdown files I own — identity, preferences,
  domains, projects. It is my canonical, portable context layer: any
  assistant can load it, and it belongs to me, not to a platform. It
  deliberately omits exact residence, family identities, and pastoral data,
  and it holds durable, high-level context only.
- **The detail layer.** **Project OCC**, a second repository, carries
  per-project tracking, attention state, and evidence — so the Context OS
  never becomes a task dump.
- **October 28, 2026.** I connected GitHub, so the agent can read my
  repositories directly and write to them only with my per-change review.
- **October 28, 2026.** I restructured the work into **side chats**: one
  main chat as personal agent and orchestrator, plus one chat per project
  area (business, ministry, websites, creative writing, Bible college, and
  later product workflow). The side chats do not share context with each
  other — which turned out to be the point. Each chat accumulates deep,
  uncontaminated context for its own project; the main chat routes work to
  the right room, keeps cross-project decisions, and runs a weekly review.
- **What I noticed.** The agent picks up new tasks quickly — not because
  the model got smarter, but because the context is pre-loaded, scoped to
  the room, and kept current.

## In plain words

- **AI agent** — an AI assistant that does work with you over time: reading
  files, using tools, remembering what it is told to keep — not just a
  chatbot answering one question at a time.
- **Personal agent** — an AI agent set up for one person: it knows your
  work, your preferences, and your projects, and acts as your assistant.
- **GitHub** — a website that stores files (especially text and code) with
  a complete history of every change, so nothing is ever truly lost and
  many hands — human or AI — can work on the same files safely.
- **Repository** — one stored project on GitHub: a folder of files plus its
  whole history.
- **Commit** — one saved change to a repository, with a note saying what
  changed. A repository is a chain of commits.
- **Context** — everything the agent knows about you and your work at the
  moment it acts. Good context, loaded in advance, is most of the magic.
- **Side chat** — a separate conversation dedicated to one project. It
  remembers its own project deeply and stays out of the others' way.
- **Orchestrator** — the main chat's job: routing each piece of work to the
  right room, and reviewing the whole picture across rooms.

Every term also lives in the [glossary](../../glossary.md).

## How it works

Picture three layers, with you on top:

```text
You — every irreversible decision stays yours
│
├── Main chat — your agent as orchestrator: routes work, reviews all of it
│     └── Side chats — one room per project, each with deep, separate context
│
└── Files you own, on GitHub
      ├── Personal Context OS — the durable layer: who you are, how you work
      └── Project OCC — the detail layer: status, tasks, evidence per project
```

The agent is only as good as what it can load. The Context OS gives it your
durable world in minutes; Project OCC gives it today's truth about each
project; the side chats give each project a room where that truth stays
uncontaminated by the others. Change any one layer without disturbing the
rest — that separation is what makes the whole thing maintainable.

## Try it yourself

The smallest version, in an afternoon:

1. **Pick one agent and give it real, reversible work** — email triage,
   scheduling, a research question. Not a toy task; real work teaches you
   both what it can do and what it gets wrong.
2. **Write a one-page context file about yourself** — who you are, what
   you're working on, how you like to work, what it must never do without
   asking. Save it somewhere you own, as plain text.
3. **Keep project details in a separate list** — one per project, apart
   from the page about you. Notice how different the two feel; that
   difference is the two-layer rule.
4. **Give each project its own conversation.** When a chat starts mixing
   projects, split it. Name the rooms so you always know where you are.

## What it proved

Six patterns, recorded in full in [patterns.md](../../patterns.md):

1. Context is infrastructure you own.
2. Separate the layers.
3. One room per project.
4. The human keeps the irreversible decisions.
5. Minimum viable complexity.
6. Verify live facts before building on them.

---

*Next in this series: Article 002 — Giving the Agent a Memory It Can Keep
(planned).*

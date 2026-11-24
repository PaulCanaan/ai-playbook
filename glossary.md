# Glossary

Every term in this playbook, in plain words. Written for a smart friend who
has never seen any of this. Terms are added the first time an article needs
them — never in bulk, ahead of need.

**AI agent** — An AI assistant that does work with you over time: reading
files, using tools, and carrying context between tasks. More than a chatbot
that answers one question and forgets it.

**AI infrastructure** — The physical and rented machinery a model runs
on: specialized chips, servers, data centers, networks, and the hosting
services that serve models through an API. Full article:
[What is AI infrastructure?](basics/what-is-ai-infrastructure.md)

**Agent loop** — The repeating cycle an agent works in: observe the
current state, decide the next step, act (often by calling a tool), and
observe the result — until the task is done or a rule stops it. Full
article: [What is an agent loop?](basics/what-is-an-agent-loop.md)

**API** — A defined set of requests one program can make of another, and
the answers it can expect back — the menu, not the kitchen. Full article:
[What is an API?](basics/what-is-an-api.md)
**Boundary** — A line the agent proposes before the person crosses it: it surfaces a conflict, names what would have to give, and asks — instead of clearing the calendar on its own.


**CLI** — A command line interface: controlling a computer by typing
precise text commands instead of clicking. Full article:
[What is a CLI?](basics/what-is-a-cli.md)

**Coding agent** — An AI agent that works on your own computer
through a command line: it reads and edits files, runs tools, and does
the mechanical parts of a job while a person directs it and approves
the steps that cannot be undone. Claude Code and Codex are the
examples used in this playbook.

**Commit** — One saved change to a repository, with a short note saying what
changed and why. A repository's history is a chain of commits; any of them
can be revisited.

**Context** — Everything the agent knows about you and your work at the
moment it acts: your identity, preferences, project state, and the
conversation so far. The quality of the context decides the quality of the
work.

**Context window** — The amount of text, counted in tokens, that a model
can hold in view at one time while it answers; anything outside it might
as well not exist for that answer. Full article:
[What is a context window?](basics/what-is-a-context-window.md)

**Dashboard** — A surface that gathers the numbers for one job — balances, budgets, totals — so the whole picture is visible at a glance. It becomes a workboard when you can act on it, not just read it.
**Debrief** — A short review after an event: what worked, what flexed, what to change — written into the standing instructions the same day, while it is still fresh.


**Embedding** — A list of numbers that stands for a piece of text by its
meaning, so that pieces with similar meanings get similar numbers and a
computer can find things by meaning instead of by matching exact words.
Full article: [What is an embedding?](basics/what-is-an-embedding.md)

**GitHub** — A website that stores files — especially text and code — with a
complete history of every change. It is the filing cabinet underneath this
whole playbook: the files live there, owned by their author, and both humans
and AI agents can work on them safely. Full article:
[What is GitHub?](basics/what-is-github.md)

**IDE** — An integrated development environment: a program that brings
together a text editor, a file browser, a terminal, and tools for running
and checking code, so writing software happens in one place. Full article:
[What is an IDE?](basics/what-is-an-ide.md)

**Inference** — Running a trained model to produce an answer: feeding it
input and letting it generate output, one token at a time. Training builds
the model; inference uses it. Full article:
[What is inference?](basics/what-is-inference.md)

**Kanban** — A way of arranging work as cards in columns: each card is one item, each column is a stage. Moving the card moves the work.

**LLM** — A large language model: a program trained on enormous amounts
of text to predict what should come next, and the engine underneath every
agent in this playbook. Full article: [What is an LLM?](basics/what-is-an-llm.md)

**Markdown** — A way of writing formatted text with simple characters —
`#` for headings, `-` for lists — in plain-text files any program can read.
This playbook, and the context files it describes, are written in Markdown.

**MCP** — The Model Context Protocol: an open standard for connecting AI
applications to tools and data through one common plug. Full article:
[What is MCP?](basics/what-is-mcp.md)

**Orchestrator** — The main chat's role in a multi-room setup: it routes
each piece of work to the right project room, keeps the cross-project
decisions, and reviews the whole picture on a rhythm.

**Obsidian** — An app for notes and knowledge that keeps everything as
plain Markdown files in a folder on your own computer, linked into a web
you own outright. Full article: [What is Obsidian?](basics/what-is-obsidian.md)
**Operations loop** — The cycle an app lives in after it ships: use it, find the failure, write the rule, use it again. The app improves by being used, not by being finished.


**Personal agent** — An AI agent set up for one person. It knows your work,
your preferences, and your projects, and acts as your ongoing assistant
rather than a stranger you re-brief every time.

**Personal Context OS** — The author's name for his durable context layer:
a private repository of curated Markdown files — identity, preferences,
domains, projects — that any assistant can load. "OS" because it works like
an operating system for the agent: the stable layer everything else runs
on.

**Prompt** — What you type (or say) to an AI to ask for something. In this
playbook the word matters less than people think: durable context and clear
structure do more work than clever prompt wording.

**RAG** — Retrieval-augmented generation: before answering, a system
retrieves relevant passages from a document collection and puts them in
the context window, so the model answers from those passages instead of
from memory alone. Full article: [What is RAG?](basics/what-is-rag.md)
**Refresh rhythm** — The schedule on which a living surface rebuilds itself from its sources: every morning, every hour, or after every change. The rhythm is part of the system, not an afterthought.
**Read-back** — Verifying a change by reading the live result afterward, not by trusting the success message. The "ok" is a claim; the read-back is the evidence.



**Repository** — One stored project on GitHub: a folder of files plus its
entire history. Often shortened to "repo."
**Rolling window** — A view that always starts today and looks forward a fixed number of days, instead of a fixed calendar week. Today first; the past drops off on its own.


**Side chat** — A separate conversation dedicated to one project or area of
life. It accumulates deep context about its own project and, by design, does
not share context with the other rooms.
**Silent failure** — A step that reports success while changing nothing: a sync that saved nothing, a call that ignored a field. Silent failures are the ones live use exists to catch.


**Skill** — A reusable, step-by-step capability packaged as files: it
teaches an AI agent how to do one job well, the same way every time.
Articles in this playbook tell the story of a lesson; a skill is the lesson
turned into a tool.
**Space** — A small web surface built for one job, fed by the records you already keep and rebuilt on a schedule, so it stays current without anyone opening it and editing it by hand.
**Standing rule** — A rule written into the agent's instructions that applies every time, until it is changed. A standing rule is how a one-time lesson becomes permanent behavior.



**Token** — The small chunk of text — often part of a word — that an LLM
reads and writes one at a time; the unit context, cost, and speed are
measured in. Full article: [What is a token?](basics/what-is-a-token.md)

**Workboard** — A living surface that shows a project's current state and lets you change it in place: move a card, flip a status, mark a task done — right on the board, without opening another file.

# Glossary

Every term in this playbook, in plain words. Written for a smart friend who
has never seen any of this. Terms are added the first time an article needs
them — never in bulk, ahead of need.

**AI agent** — An AI assistant that does work with you over time: reading
files, using tools, and carrying context between tasks. More than a chatbot
that answers one question and forgets it.

**Agent loop** — The repeating cycle an agent works in: observe the
current state, decide the next step, act (often by calling a tool), and
observe the result — until the task is done or a rule stops it. Full
article: [What is an agent loop?](basics/what-is-an-agent-loop.md)

**API** — A defined set of requests one program can make of another, and
the answers it can expect back — the menu, not the kitchen. Full article:
[What is an API?](basics/what-is-an-api.md)

**CLI** — A command line interface: controlling a computer by typing
precise text commands instead of clicking. Full article:
[What is a CLI?](basics/what-is-a-cli.md)

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

**GitHub** — A website that stores files — especially text and code — with a
complete history of every change. It is the filing cabinet underneath this
whole playbook: the files live there, owned by their author, and both humans
and AI agents can work on them safely. Full article:
[What is GitHub?](basics/what-is-github.md)

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

**Repository** — One stored project on GitHub: a folder of files plus its
entire history. Often shortened to "repo."

**Side chat** — A separate conversation dedicated to one project or area of
life. It accumulates deep context about its own project and, by design,
does not share context with the other rooms.

**Skill** — A reusable, step-by-step capability packaged as files: it
teaches an AI agent how to do one job well, the same way every time.
Articles in this playbook tell the story of a lesson; a skill is the lesson
turned into a tool.

**Token** — The small chunk of text — often part of a word — that an LLM
reads and writes one at a time; the unit context, cost, and speed are
measured in. Full article: [What is a token?](basics/what-is-a-token.md)

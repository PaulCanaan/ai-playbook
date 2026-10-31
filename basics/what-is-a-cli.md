---
title: "What Is a CLI?"
type: basics
stage: 1
date: 2026-10-30
status: Living
related: [what-is-an-api, what-is-mcp]
---

# What Is a CLI?

## In one sentence

A CLI — a *command line interface* — is a way of controlling a computer by
typing precise text commands instead of clicking buttons.

## In plain words

Most software you know has a **graphical** interface: windows, buttons,
menus — a GUI. A CLI is the older, plainer sibling: you type a command
into a text window called a *terminal*, press Enter, and the computer does
exactly that and answers in text.

`ls` — list the files here. `cd photos` — go into the photos folder.
`mkdir garden` — make a folder called "garden." Verb, then details. That
is nearly the whole grammar.

It looks austere. It is also exact: a typed command says precisely what to
do, can be written down, repeated a thousand times without drifting, and
combined with other commands like building blocks.

## A tiny example

To find every file in a folder whose name mentions "monstera," a person
clicks and scrolls. A CLI user types one line:

```text
ls | grep monstera
```

"List the files, and keep only the lines mentioning monstera." Two small
commands, chained. Much of the automation in this playbook is, underneath,
agents chaining small commands like this.

## Why it matters in this playbook

Agents are fluent in text — and a CLI *is* text. So a great deal of what an
agent does in this playbook arrives as CLI work: the tools that read email,
check calendars, search repositories, and monitor marketplaces are
command-line tools the agent runs and reads. When the playbook says "the
agent checked GitHub," very often a CLI command was typed and its text
output was read.

This is also why CLI skills are worth a beginner's hour: once you can read
a command, you can read much of what your agent is doing — and catch it
before it does the wrong thing.

## Common confusions

- **The terminal is not the CLI.** The terminal is the window; the CLI is
  the language spoken in it — the commands of whatever program you are
  talking to.
- **CLI is not "programming."** It is operating: telling the computer to do
  things, not writing new software. (Though scripts — saved lists of
  commands — are where the two meet.)
- **Newer is not always better.** GUIs are kinder for exploring; CLIs win
  on precision, repetition, and record-keeping — the things agent work is
  made of.

## Go deeper

- [What is an API?](what-is-an-api.md) — the other way programs (and
  agents) ask for things.
- The [resources library](../resources/README.md) — several tools there
  are driven from the command line.

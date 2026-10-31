---
title: "What Is an API?"
type: basics
stage: 1
date: 2026-10-30
status: Living
related: [what-is-a-cli, what-is-mcp, what-is-an-llm]
---

# What Is an API?

## In one sentence

An API — an *application programming interface* — is a defined set of
requests one program can make of another, and the answers it can expect
back.

## In plain words

Picture a restaurant. You do not walk into the kitchen and cook; you order
from a menu, the kitchen prepares it, and a waiter brings exactly what the
menu promised. The **menu** is the API: a fixed list of what may be asked
for, in what form, and what will come back.

Software works the same way. A weather service offers an API: send it a
request — "weather for Denver, tomorrow" — in the agreed format, and it
returns the forecast in an agreed format. Your email app, your calendar,
your bank: nearly every service you use offers one, and nearly everything
programs do *for each other* travels through one.

Two more pieces of the picture:

- **Requests and responses.** Every API interaction is: a request goes out
  ("get," "create," "send"), a response comes back — data, or a
  confirmation, or an error saying precisely why not.
- **Keys and permissions.** Most APIs ask *who is asking*, via an API key
  or a sign-in. The key carries permissions — read-only, or read-and-write
  — which is how a service lets your agent look at your calendar without
  being able to spend your money.

## A tiny example

When this playbook's agent checks what is on your calendar, somewhere
underneath there is a request much like:

```text
GET /calendars/primary/events?from=2026-11-01
→ 200 OK: [ { "title": "Group Leader Dinner", "starts": "18:30" }, … ]
```

A question in a fixed format; an answer in a fixed format. Multiply by
every service you own, and you have most of what "connected" software is.

## Why it matters in this playbook

APIs are how an agent *acts* rather than merely talks. Reading your email,
searching a repository, placing a hold on a calendar — each is an API call
someone designed to be safe for programs to make. The playbook's guardrail
pattern (the human keeps the irreversible decisions) is enforced right
here: the dangerous calls — send, buy, publish, delete — are exactly the
ones the owner approves before the agent makes them.

APIs are also why the [CLI](what-is-a-cli.md) matters: many of the tools in
this playbook are thin, readable wrappers that turn a typed command into
the right API request.

## Common confusions

- **An API is not an app.** It is the doorway, not the building. The same
  calendar service can serve a phone app, a website, and your agent —
  through the same API.
- **"There's no API for that" is a real limit.** If a service offers no
  doorway, an agent can only use the front door like a human would — the
  website — slowly and fragilely. Much of practical AI work is checking
  which doorways exist.
- **A key is a credential.** Whoever holds your API key can act as you,
  within its permissions. Keys are stored in vaults, never pasted into
  chats or files.

## Go deeper

- [What is MCP?](what-is-mcp.md) — the standard that packages tools and
  APIs for agents.
- [OpenAI Cookbook](../resources/README.md) — API use, in worked examples.

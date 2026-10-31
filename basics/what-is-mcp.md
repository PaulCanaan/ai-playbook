---
title: "What Is MCP?"
type: basics
stage: 1
date: 2026-10-30
status: Living
related: [what-is-an-api, what-is-a-cli]
---

# What Is MCP?

## In one sentence

MCP — the *Model Context Protocol* — is an open standard that lets AI
applications connect to external tools and data through one common plug,
instead of a custom wire for every tool.

## In plain words

Before USB, every device had its own cable and every computer its own
ports. MCP aims to be the USB-C of AI tools — an analogy its creators use
themselves.

The problem it solves: an agent becomes useful when it can reach your
email, files, calendar, and databases. Without a standard, every AI app
must hand-build a connection to every service — the same work, redone by
everyone. With MCP, a service (or a fan of it) builds one **MCP server**
that offers its tools and data in the standard shape, and **any** AI
application that speaks MCP can use it.

The cast, in plain words:

- **MCP server** — a small program that offers a set of tools ("search
  messages," "list events," "read this file") and data, in the standard
  format. One server per service, roughly.
- **MCP client / host** — the AI application (the agent's home) that
  connects to servers and presents their tools to the model.
- **Tools** — the callable actions themselves, each with a name, a
  description the model can understand, and a defined input and output.

## A tiny example

Connect a GitHub MCP server to your agent, and the agent gains tools like
"search repositories" and "read file" — described in a form it can
reliably choose and call. This very playbook was built that way: its
articles and pull requests traveled through GitHub's MCP server, called
from an agent that never saw a password.

## Why it matters in this playbook

MCP is the connection layer of the architecture in
[Article 001](../articles/series-1-the-personal-agent/001-onboarding-a-personal-agent.md).
The playbook's agent reads email, checks calendars, works in repositories,
and watches marketplaces — not by magic, but through connectors built on
ideas like this one. When you evaluate any new AI tool, "does it speak
MCP, or offer servers?" is now one of the most practical questions you can
ask: it decides how much of your world the tool can reach.

## Common confusions

- **MCP is not a model, and not an agent.** It is plumbing — a protocol.
  The model still decides; MCP just standardizes how its chosen tools are
  offered and called.
- **MCP is not the same as an [API](what-is-an-api.md).** APIs are how a
  service exposes itself; MCP is a standard way to *package* tools (often
  built on those APIs) so any AI app can use them without custom work.
- **Connecting a server is a trust decision.** A server's tools act with
  *your* permissions. Connect servers the way you would hand out keys —
  which is why this playbook approves consequential actions individually.

## Go deeper

- [MCP Servers](../resources/README.md) — the reference collection of
  servers to browse.
- [What is a CLI?](what-is-a-cli.md) — the other, older way agents drive
  tools.

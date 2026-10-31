---
title: "What Is GitHub?"
type: basics
track: tools
stage: 1
date: 2026-10-30
status: Living
related: [what-is-a-cli, what-is-an-api]
---

# What Is GitHub?

## In one sentence

GitHub is a website where files — especially text and code — are stored
with a complete, permanent history of every change, so people and AI
agents can work on them together without ever truly breaking anything.

## In plain words

Underneath GitHub sits **Git**, a tool programmers use to track versions
of files: every change is saved as a [commit](../glossary.md) with a note
saying what changed, and the whole history can be revisited, compared, or
restored. GitHub takes Git and gives it a home on the internet, with a
friendly face: web pages for browsing the files and their history,
discussing changes, and proposing new ones.

Three pieces of vocabulary carry most of it:

- **Repository** — one project: a folder of files plus its entire history.
  This playbook is a repository.
- **Branch** — a parallel copy of the project where changes can be drafted
  safely, without touching the official version (called **main**).
- **Pull request (PR)** — a proposal: "here is what I changed on my branch,
  and why — please review and merge it into main." Merging a PR makes the
  change official.

That draft → propose → review → merge rhythm is why GitHub suits agent
work so well: an agent can do real work in the open, and a human can see
every line before it lands.

## A tiny example

This playbook's own history is the example. Its first articles arrived as
direct commits. Then its owner began an experiment: changes now arrive as
pull requests — one proposed the repository's scope rule, one its
knowledge base, one its basics articles — each readable, each reversible,
each merged only after checks passed. You can open any repository and read
its story in its commits and pull requests; nothing is hidden.

## Why it matters in this playbook

GitHub is the filing cabinet underneath the whole architecture in
[Article 001](../articles/series-1-the-personal-agent/001-onboarding-a-personal-agent.md):
the Personal Context OS is a repository, the project tracker is a
repository, this playbook is a repository. Files you own, in plain text,
with history — [Pattern 1](../patterns.md) made practical.

It is also where your agent will increasingly *work*: through GitHub's
[API](what-is-an-api.md) and [MCP](what-is-mcp.md) server, an agent can
read repositories, propose changes as pull requests, and — where the owner
allows it — merge them, all without ever holding your password.

## Common confusions

- **Git is not GitHub.** Git is the version-tracking tool (it works fully
  offline, on your own machine). GitHub is one — the largest — of the
  websites that host Git repositories and add collaboration around them.
- **A repository is not just backup.** Backup saves copies; GitHub keeps
  the *story* — who changed what, when, and why — and lets many hands,
  human and AI, change things in parallel without colliding.
- **Public is a choice, not the default fate.** Repositories can be
  private. This playbook is private while it grows, and written to be
  shareable later — see its Scope rule.

## Go deeper

- [What is a CLI?](what-is-a-cli.md) — Git is often driven from the
  command line.
- [What is MCP?](what-is-mcp.md) — how agents connect to GitHub without
  passwords.

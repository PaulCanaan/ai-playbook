---
title: "What Is an LLM?"
type: basics
stage: 1
date: 2026-10-30
status: Living
related: [what-is-a-token, what-is-an-api, what-is-mcp]
---

# What Is an LLM?

## In one sentence

An LLM — a *large language model* — is a program trained on enormous
amounts of text that has learned to predict, very well, what word-piece
should come next.

## In plain words

Imagine autocomplete on your phone, after it has read much of the public
internet, millions of books, and mountains of code. Given some text, it
does not look answers up in a database; it *continues the text* in the most
plausible way, one small piece at a time (those pieces are
[tokens](what-is-a-token.md)).

That sounds too simple to produce the conversations you have with an AI
assistant — but prediction at this scale turns out to require something
like understanding. To predict text well, the model had to absorb grammar,
facts, reasoning patterns, styles, and the shapes of arguments and stories.
Nobody programmed those in one by one; they emerged from the training.

"Large" refers to the model's size — billions of internal settings, tuned
during training — and to the scale of text it learned from.

## A tiny example

Give an LLM: *"The capital of France is"* — and the most plausible next
token is " Paris". Give it a question, and the most plausible continuation
is an answer. Give it your half-written email and a request to make it
kinder, and the most plausible continuation is the kinder version. Same
mechanism, every time: read everything so far, predict what comes next,
repeat.

## Why it matters in this playbook

The LLM is the *engine* underneath everything here. Your
[personal agent](../articles/series-1-the-personal-agent/001-onboarding-a-personal-agent.md)
is an LLM plus the things this playbook adds around it: your
[context](../glossary.md), tools it can use through [APIs](what-is-an-api.md)
and [MCP](what-is-mcp.md), and instructions for how to behave. Understanding
that the engine is a predictor explains both its brilliance and its failure
modes — which is most of working with AI well.

## Common confusions

- **It is not a database.** It does not store and retrieve documents; it
  generates text. That is why it can be fluent and wrong in the same
  sentence — always verify facts that matter.
- **It does not remember you between conversations.** Anything it "knows"
  about you in a session was loaded into that session — which is exactly
  why this playbook treats context as files you own.
- **It is not the whole agent.** An LLM alone predicts text. An agent is
  what happens when you give that engine context, tools, and a job.

## Go deeper

- [Dive into LLMs](../resources/README.md) — hands-on tutorials on how
  these models work, in code.
- [AI for Beginners](../resources/README.md) — the gentle full curriculum.
- Next basic: [What is a token?](what-is-a-token.md)

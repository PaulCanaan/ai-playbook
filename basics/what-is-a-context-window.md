---
title: "What Is a Context Window?"
type: basics
stage: 1
date: 2026-10-30
status: Living
related: [what-is-a-token, what-is-an-llm]
---

# What Is a Context Window?

## In one sentence

A context window is the maximum amount of text — counted in
[tokens](what-is-a-token.md) — that a model can hold in view at one time
while it produces an answer.

## In plain words

Think of the model as a very capable reader with a desk of a fixed size.
Everything it is allowed to consider has to fit on that desk: the
instructions it was given, the conversation so far, any files or passages
loaded for it, the results of any tools it called, and the answer it is
in the middle of writing.

Anything that does not fit on the desk does not exist for the model in
that moment. It has not "forgotten" it the way a person forgets — it
simply cannot see it. To use something again, it has to be put back on
the desk: pasted in, loaded from a file, or retrieved.

Window sizes are measured in tokens and keep growing — from a few
thousand in early models to hundreds of thousands, even a million, in
current ones. But no window is infinite, and bigger is not free: more
tokens in view means more cost, more waiting, and more noise competing
for the model's attention.

## A tiny example

Start a long conversation about a project. In the first message you
explain a key decision. Fifty messages later, after long documents and
tool results have filled the window, that first message may no longer be
in view — and the assistant answers as if the decision was never made.
Nothing broke. The desk filled up, and the first page slid off.

That failure has an engineering answer, and this playbook is largely
about it: write the decision down in a file you own, and load the file
when it matters, instead of relying on the conversation to remember.

## Why it matters in this playbook

The context window is the physical reason behind the architecture in
[Article 001](../articles/series-1-the-personal-agent/001-onboarding-a-personal-agent.md):

- **Context files are kept tight and layered** because every line spends
  window. Curated context beats complete context.
- **One room per project** works partly because each room loads only its
  own context, instead of every project competing for one desk.
- **Memory lives in files, not in chats,** because files can be put back
  on the desk any time; an old conversation cannot.
- **Retrieval** — see [What is RAG?](what-is-rag.md) — exists to choose
  *which* pages go on the desk, out of a library far too big to fit.

## Common confusions

- **The context window is not the model's knowledge.** What the model
  learned in training is in its weights; the window is only what it is
  *looking at* right now. A model can "know" a fact in general and still
  miss the specific one in your project that never made it into the
  window.
- **A bigger window does not remove the need to curate.** A desk piled
  with everything is not the same as a desk arranged with what matters.
  Relevance, order, and clarity still decide how well the model uses
  what it can see.
- **When an assistant "forgets," it is usually a window problem, not a
  character flaw.** The fix is structural — load the right file — not
  repeating yourself louder.

## Go deeper

- [What is a token?](what-is-a-token.md) — the unit the window is
  measured in.
- [What is RAG?](what-is-rag.md) — how systems choose what enters the
  window from a large library.
- [Dive into LLMs](../resources/README.md) — context and attention,
  hands-on in code.

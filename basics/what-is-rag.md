---
title: "What Is RAG?"
type: basics
stage: 4
date: 2026-10-30
status: Living
related: [what-is-a-context-window, what-is-an-llm]
---

# What Is RAG?

## In one sentence

RAG — *retrieval-augmented generation* — is a technique where a system
first **retrieves** relevant passages from a collection of documents and
places them in the model's [context window](what-is-a-context-window.md),
so the model answers from those passages instead of from memory alone.

## In plain words

An [LLM](what-is-an-llm.md) answering from training alone is like a
student writing an exam from memory: often good, sometimes confidently
wrong, and it knows nothing about *your* documents — they were never in
its training. RAG turns the closed-book exam into an open-book one.

It works in two halves:

1. **Retrieval.** Before the model is asked anything, the system takes
   your question, searches a prepared collection — your files, notes, a
   manual, a knowledge base — and pulls out the handful of passages most
   relevant to it. The collection is usually split into small chunks in
   advance, and each chunk is indexed so it can be found by meaning, not
   only by exact keywords.
2. **Generation.** Those passages are placed into the context window
   alongside your question, and the model writes its answer *using
   them* — ideally citing or sticking close to what they actually say.

The model is not retrained and learns nothing permanent. Tomorrow, with
different passages retrieved, it answers differently. The knowledge lives
in the collection; the model borrows it for one answer at a time.

## A tiny example

You keep a notebook of decisions for a project and ask, "Why did we
choose the cheaper supplier?" A RAG system searches the notebook, finds
the paragraph where the decision and its reasons were recorded, puts
that paragraph in front of the model, and the answer comes back with
your reasons — not a generic guess about why people usually choose cheap
suppliers. Without retrieval, the model would have had to invent an
answer, fluently.

## Why it matters in this playbook

RAG is the bridge between Pattern 1 — context is infrastructure you own —
and a library too big to load whole:

- Your files stay **yours, in plain text, editable**; RAG is how an agent
  uses a growing library without anyone pasting it all into a chat.
- It explains tools like AnythingLLM in the [learning path](../learning-path.md)
  (Stage 4): connect your own documents, ask questions, get answers drawn
  from them.
- It is also how a personal agent's memory works at scale. A small set of
  core files can be loaded in full; everything beyond that has to be
  *found when relevant* — which is retrieval by another name.

And it sets an expectation: a RAG answer is only as good as what was
retrieved. If the right passage was never written down, or the search
missed it, the model answers from the wrong page with the same fluency.
That is why this playbook treats writing things down — clearly, once, in
the right place — as load-bearing work.

## Common confusions

- **RAG is not training.** Nothing is added to the model. Edit the
  document and the next retrieved answer uses the edit; delete it and
  the "knowledge" is gone. That is a feature: your information stays
  under your control.
- **RAG is not a truth guarantee.** Retrieval improves the odds and
  grounds the answer in sources you can check, but the model can still
  misread a passage, and a wrong passage retrieved confidently is worse
  than no passage. Sources you can open and verify are part of the
  design, not a decoration.
- **RAG is not just search.** A search engine returns documents for a
  *person* to read. RAG retrieves passages for a *model* to use
  mid-answer — the retrieval step serves the generation step, which is
  exactly what the name says.

## Go deeper

- [What is a context window?](what-is-a-context-window.md) — the space
  retrieved passages are placed into, and why choosing them matters.
- [AnythingLLM](../resources/README.md) — RAG over your own documents,
  ready to run.
- [What is an embedding?](what-is-an-embedding.md) — how "find by meaning" actually works, and the step underneath RAG's retrieval.

---
title: "What Is an Embedding?"
type: basics
stage: 4
date: 2026-10-30
status: Living
related: [what-is-rag, what-is-a-context-window, what-is-an-llm]
---

# What Is an Embedding?

## In one sentence

An embedding is a list of numbers that stands for a piece of text by its
meaning, so that pieces with similar meanings get similar numbers — which
lets a computer find things by meaning instead of by matching exact words.

## In plain words

Keyword search matches letters. Ask for "dog" and it finds "dog"; it
misses "puppy" and "canine" unless someone told it those words are
related. An embedding takes a different route: it turns a piece of text
— a sentence, a paragraph, a whole page — into a point on a map.

Think of it as coordinates. A model trained for this job reads the text
and produces a long list of numbers, called a vector. Texts that mean
similar things land near each other on the map; texts that mean
different things land far apart. "Dog" and "puppy" end up close together
even though they share no letters, because the model has seen both used
in similar ways. "Dog" and "democracy" end up far apart.

Once every chunk of a collection has its coordinates, finding becomes
measuring distance: take the question, turn it into coordinates the same
way, and look for the chunks nearest to it. That is how "find by
meaning" actually works, and it is the step underneath
[RAG](what-is-rag.md)'s retrieval — the reason a RAG system can pull out
the right paragraph even when it uses none of the question's words.

A few details that matter for intuition, not for memorization:

- **The numbers are learned, not assigned.** Nobody writes a rule saying
  "dog = 0.7". An embedding model learns the map from vast amounts of
  text, by noticing which words and passages appear in similar
  contexts.
- **Similarity is a matter of degree.** Two chunks can be a little
  similar, very similar, or unrelated — there is no yes-or-no boundary,
  only distance on the map.
- **The same text can be embedded more than once.** A short chunk and a
  long document containing it get different coordinates, because they
  mean different amounts of things. That is one reason RAG systems split
  documents into small chunks before embedding them.

## A tiny example

You keep a folder of how-to notes and ask, "How do I fix a leaking
tap?" A keyword search finds only notes containing "leaking" or "tap".
An embedding search turns your question into coordinates, measures the
distance to every note's coordinates, and returns the note titled "Stop
a dripping faucet" — it shares no word with your question, but it means
the same thing, so it lands nearby on the map.

## Why it matters in this playbook

Embeddings are the quiet machinery behind two things this playbook
relies on:

- **RAG, in Stage 4 of the [learning path](../learning-path.md).** When
  a system retrieves passages from your documents instead of answering
  from memory, embeddings are usually how it chooses which passages to
  retrieve. Understanding them tells you why retrieval sometimes misses:
  a passage can be genuinely relevant and still land far from the
  question on the map, if the wording points elsewhere.
- **Search that understands.** Any tool that promises to "search by
  meaning" — over notes, manuals, or a knowledge base — is almost
  certainly embedding the collection and measuring distance. Once you
  know that, you can judge the claim: it will be good at near-misses of
  wording, and weak wherever meaning depends on details the map
  smooths over.

It also explains a practical habit: writing things down in small, clear,
self-contained chunks. A chunk that says one thing cleanly gets
coordinates that mean one thing — and is found when it matters.

## Common confusions

- **An embedding is not a summary.** A summary is shorter text you can
  read. An embedding is a list of numbers you cannot read at all; its
  only use is measuring how close two pieces of text are in meaning.
- **An embedding is not understanding.** The model does not know what a
  dog is. It has learned that "dog" behaves like "puppy" in text. The
  map is a pattern of usage, not a picture of the world — which is why
  it can be confidently wrong about things that look alike in wording
  but differ in fact.
- **An embedding is not permanent knowledge.** Change the embedding
  model and every coordinate changes, because the map is redrawn. The
  text itself stays yours and readable; the numbers are a derived index
  you can always rebuild.
- **An embedding is not the same as a token.** A
  [token](what-is-a-token.md) is the small chunk of text a model reads
  and writes. An embedding is the numbers a model assigns to a chunk of
  text to place it on the meaning map. Tokens are the input; embeddings
  are a measurement made from it.

## Go deeper

- [What is RAG?](what-is-rag.md) — the technique embeddings power: retrieve
  first, then generate from what was retrieved.
- [What is a context window?](what-is-a-context-window.md) — the space the
  retrieved passages are placed into.
- [What is an LLM?](what-is-an-llm.md) — the prediction engine that sits
  behind both the embedding model and the answering model.
- [AnythingLLM](../resources/README.md) — RAG over your own documents,
  with embeddings doing the finding underneath.

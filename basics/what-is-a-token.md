---
title: "What Is a Token?"
type: basics
stage: 1
date: 2026-10-30
status: Living
related: [what-is-an-llm]
---

# What Is a Token?

## In one sentence

A token is the small chunk of text — often part of a word — that an
[LLM](what-is-an-llm.md) reads and writes, one chunk at a time.

## In plain words

LLMs do not read letter by letter, and not quite word by word either. Text
is first chopped into tokens by a fixed chopping scheme: common words are
one token, rarer words split into pieces, punctuation and spaces attach to
what follows them.

A rough rule for English: **one token ≈ four characters, or about
three-quarters of a word.** So 100 tokens ≈ 75 words; this whole article is
roughly 400 tokens. In Chinese, a single character is often about one
token in modern models, so the same meaning can cost a different number of
tokens in different languages.

## A tiny example

The sentence *"I love gardening"* might chop into three tokens —
"I", " love", " gardening". A longer word like *"photosynthesis"* might
split into two or three pieces — "photo", "synthesis" — because the model
keeps common *pieces*, not a dictionary of whole words.

## Why it matters in this playbook

Tokens are the unit everything is measured in:

- **Context windows** — how much an agent can hold in mind at once — are
  counted in tokens. When this playbook says "load your context," it means
  spending tokens from a finite budget. That is the practical reason
  context files are kept tight and layered.
- **Cost and speed** are counted in tokens: you pay, and wait, per token
  read and written.
- **Why agents forget mid-conversation:** when a conversation outgrows
  the window, the oldest tokens fall away. Files you own do not fall away
  — another reason the playbook's memory lives in files.

## Common confusions

- **A token is not a word.** Sometimes it is a word, sometimes a fragment,
  sometimes just a space and a comma. Any word-count estimate is a
  translation, not an equality.
- **More tokens is not automatically better context.** A window stuffed
  with irrelevant text spends the budget and dilutes the signal. Curated
  beats complete — a rule this playbook applies everywhere.

## Go deeper

- [What is an LLM?](what-is-an-llm.md) — the engine that consumes tokens.
- [Dive into LLMs](../resources/README.md) — tokenization in code, hands-on.

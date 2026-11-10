---
title: "What Is Inference?"
type: basics
stage: 4
date: 2026-11-10
status: Living
related: [what-is-an-llm, what-is-ai-infrastructure, what-is-a-token]
---

# What Is Inference?

## In one sentence

Inference is running a trained model to get an answer — feeding it input and letting it produce output — as opposed to training, which is building the model in the first place.

## In plain words

Training is school; inference is the job. A model spends its training learning patterns from enormous amounts of text, and all of that learning is frozen into the finished model. Inference is what happens every time you actually use it: you give it some input, it runs its calculations, and it produces an answer.

Think of a chef. Years of practice taught her how flavors work, but no dinner is cooked during training. Each dinner she cooks afterward — reading the order, choosing ingredients, producing the dish — is the performance. Training built the skill; inference is the skill at work, one meal at a time.

For a language model, the performance is generating text one [token](what-is-a-token.md) at a time. You send your words, the model predicts the next token, then the next, then the next, until the answer is complete. That is why answers stream in word by word instead of arriving all at once: you are watching inference happen live.

A few things follow from seeing it this way:

- **Inference is where the cost lives.** Training is expensive once; inference is charged every time, usually per token in and out. Each question you ask is a small purchase of compute.
- **Inference is where the waiting lives.** The model can only generate so fast, and bigger models generate more slowly, because each token costs more calculation. A slow answer is usually an inference bottleneck, not a model that is "thinking hard."
- **Inference is a single run, not a memory.** Each inference call starts from the model as trained plus whatever you put in the [context window](what-is-a-context-window.md). Nothing from the last call carries over unless you put it in the context again.

## A tiny example

You ask an assistant to translate one sentence into Spanish. Your words travel to the machine running the model — a hosted [LLM](what-is-an-llm.md) on a provider's servers, or a small model on your own laptop. The model reads your sentence, then generates the translation one token at a time, streaming it back to you as it goes. The whole exchange takes a second or two.

Ask it to translate a whole book and the shape is identical, only longer: thousands of inference steps, thousands of tokens, and a bill to match. Same act, larger scale.

## Why it matters in this playbook

Nearly everything in this playbook is inference, repeated:

- **Every answer is an inference run.** When an assistant summarizes a document, drafts an email, or reviews a plan, a model is running inference on your words. Cost, speed, and privacy all live at this layer: hosted inference is fast and capable but your words leave your machine; local inference keeps them home but runs a smaller model more slowly.
- **An agent loop is inference in a cycle.** In Stage 2's [agent loop](what-is-an-agent-loop.md), each step — observe, decide, act — is another inference call. A task that takes twenty steps costs twenty runs. Knowing this is what makes you design loops that stop, instead of loops that wander.
- **Streaming is inference made visible.** Answers arrive word by word because the model generates one token at a time. When the stream stalls, inference is stalled — the model, the machine, or the network — and that tells you where to look.
- **Better input beats a bigger model, per run.** Since each inference call starts from the model plus your context, the context you supply is the cheapest lever you have. A clear brief and good files improve every run without changing the model at all.

## Common confusions

- **Inference is not learning.** The model does not learn from your conversation. Its weights — what training built — stay fixed while it answers you. It can use what you put in the context window, but when the call ends, that knowledge goes with it.
- **Inference is not thinking.** A model generating an answer is predicting the next token, not reasoning the way a person does. A fluent answer can be confidently wrong, because fluency is a property of the prediction, not a guarantee of truth.
- **Faster inference does not mean smarter answers.** Speed comes from the machinery — smaller models, better chips, more parallel capacity. Answer quality comes from the model and the context you give it. A fast wrong answer is still wrong.
- **Inference is not the same as training, even when the words overlap.** "The model was trained on the internet" describes the past; "the model is running" describes now. Confusing the two leads to the two most common mistakes: expecting a model to know things it was never trained on, and expecting it to remember what you told it last week.

## Go deeper

- [What is an LLM?](what-is-an-llm.md) — the prediction engine that inference runs.
- [What is AI infrastructure?](what-is-ai-infrastructure.md) — the chips, data centers, and hosting that inference runs on.
- [What is a token?](what-is-a-token.md) — the unit inference is measured and billed in.
- [What is an agent loop?](what-is-an-agent-loop.md) — inference repeated in a cycle, with tools and memory between runs.
- [What is RAG?](what-is-rag.md) — inference with retrieved passages added to the context first.

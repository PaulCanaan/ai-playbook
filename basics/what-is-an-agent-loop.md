---
title: "What Is an Agent Loop?"
type: basics
stage: 2
date: 2026-10-30
status: Living
related: [what-is-an-llm, what-is-mcp]
---

# What Is an Agent Loop?

## In one sentence

An agent loop is the repeating cycle — observe, decide, act, and observe
the result — that turns a model which only answers into an agent which
works through a task step by step.

## In plain words

An [LLM](what-is-an-llm.md) by itself does one thing: given text, it
produces the next text. Ask, and it answers — once. That alone cannot
check a calendar, notice a mistake, or fix what a tool just reported.

The loop wraps the model in a cycle:

1. **Observe.** The agent takes in the current state: your request,
   the conversation, file contents, or the result of the last tool call —
   all assembled into its [context window](what-is-a-context-window.md).
2. **Decide.** The model reasons over that state and chooses the next
   step: answer, ask, or call a tool — and which tool, with what inputs.
3. **Act.** The step is actually carried out: a tool runs through an
   [API](what-is-an-api.md) or [MCP](what-is-mcp.md), a file is written,
   a message is sent. This is the moment the agent touches the world.
4. **Observe the result, and repeat.** The outcome — success, error, new
   information — goes back into context, and the cycle turns again. The
   loop ends when the task is done, when a rule says stop, or when a
   human needs to decide.

Every real agent framework, whatever its name, is this cycle with
different furniture around it: how many turns are allowed, what the agent
may do without asking, what gets remembered between turns.

## A tiny example

Task: "Open a pull request with the new article." Turn by turn: the
agent *observes* the repository's current state; *decides* to create a
branch; *acts*. It *observes* the branch exists; *decides* to add the
file; *acts*. It *observes* the checks pass; *decides* the work is ready;
*acts* — the PR is opened. Then the loop reaches a gate: merging is
someone else's decision, so the loop stops and reports. One request,
many turns, each turn cheap to verify.

## Why it matters in this playbook

The agent in [Article 001](../articles/series-1-the-personal-agent/001-onboarding-a-personal-agent.md)
is this loop, running inside rules:

- **Guardrails live inside the loop.** Approval gates work because the
  loop has an *act* step that can be paused: "prepare anything, but stop
  before the irreversible action and ask." Pattern 4 — the human keeps
  the irreversible decisions — is a statement about where the loop is
  allowed to turn on its own.
- **Context design *is* loop design.** What the agent can observe decides
  what it can decide well. The layered context files, the project rooms,
  and retrieval are all ways of stocking step 1.
- **Loops need exits.** A loop without a stop condition, a turn budget,
  or an escalation path will happily work forever — or repeat the same
  failing action. Naming "done," and naming "ask the human," are part of
  building the agent, not an afterthought.

## Common confusions

- **The loop is not the model "thinking longer."** A single long answer
  still touches nothing. The loop is what lets each step be checked
  against reality — a real tool result, a real error — before the next
  step builds on it.
- **A loop is not unlimited autonomy.** The same cycle can run with a
  human approving every act, or with wide freedom on reversible work and
  hard stops elsewhere. Autonomy is a setting on the loop, not a
  property of the model.
- **More turns is not always better.** Each turn costs tokens, time, and
  a chance to wander. Good agent design is often a *smaller* loop with
  better observations — not a bigger one.

## Go deeper

- [What is MCP?](what-is-mcp.md) — how the *act* step reaches tools in a
  standard way.
- [AI Agent Book](../resources/README.md) — loops, planning, and memory,
  treated properly.
- [LangGraph](../resources/README.md) — loops made explicit as graphs,
  with state and approval gates, when your own agents outgrow the simple
  cycle.

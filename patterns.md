# Patterns

The distilled principles of this playbook — its conclusions. A pattern is
recorded here only after an article has proved it in real work, and each one
links back to that article. This page is the short version of the whole
journey.

## Pattern 1 — Context is infrastructure you own

Keep the canonical version of what your agent knows in files you control —
plain text, in a repository with history — so it is portable across tools
and models, and never hostage to one app.
*Proved by [Article 001](articles/series-1-the-personal-agent/001-onboarding-a-personal-agent.md).*

## Pattern 2 — Separate the layers

Durable context (who I am, how I work) is not project detail (status, tasks,
evidence). Keep them in different homes; mixing them bloats both until
neither loads well.
*Proved by [Article 001](articles/series-1-the-personal-agent/001-onboarding-a-personal-agent.md).*

## Pattern 3 — One room per project

Isolated context per project beats one giant thread. Give each project its
own conversation, and let an orchestrator route work and review across
rooms.
*Proved by [Article 001](articles/series-1-the-personal-agent/001-onboarding-a-personal-agent.md).*

## Pattern 4 — The human keeps the irreversible decisions

The agent drafts, researches, and prepares. Sending, buying, publishing,
and committing stay behind the owner's explicit approval.
*Proved by [Article 001](articles/series-1-the-personal-agent/001-onboarding-a-personal-agent.md).*

## Pattern 5 — Minimum viable complexity

A system that adds management burden has failed, however elegant it looks.
Every layer, file, and process must earn its maintenance cost. (A
twelve-part write-back scheme for the Context OS was retired on 2026-10-28
for exactly this reason.)
*Proved by [Article 001](articles/series-1-the-personal-agent/001-onboarding-a-personal-agent.md).*

## Pattern 6 — Verify live facts before building on them

Stale records are the most common failure mode. A fact that is old,
load-bearing, and cheap to check gets checked against the live source
before anything is built on it.
*Proved by [Article 001](articles/series-1-the-personal-agent/001-onboarding-a-personal-agent.md).*

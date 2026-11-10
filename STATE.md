# STATE — where things stand

*For agents: read this after AGENTS.md. Update it at the end of every
working session, in the same commit as the work it describes when
practical.*

## Current state (2026-11-10)

- Repository created by Paul on 2026-10-30 and seeded the same day with the
  v3 structure he approved: frame (AGENTS.md, README.md, index.json,
  templates), Article 001, glossary, patterns, and the skills shelf.
- **Series 1 — The Personal Agent:** Article 001 published (Living).
  Article 007 (Onboarding Someone Else) published out of order on
  2026-11-03 — a second person onboarded, written the week it
  happened. Articles 002–006 remain planned (titles in index.json).
- **Series 2–4:** named and described in index.json and the README; no
  articles published yet. The first Series 2 article is now planned
  (Article 008, title in index.json). Series folders are created when
  their first article lands.
- **Skills:** none published. skills/README.md explains the shelf and the
  publishing rule.
- **Basics:** the concept layer is live — basics/ holds thirteen articles
  in two tracks (concepts: LLM, token, context window, CLI, API, MCP,
  agent loop, RAG, embedding, AI infrastructure, inference; tools: GitHub, Obsidian)
  plus an index; the glossary and learning path link to them. One more
  is planned: What is an IDE? (tools track, queued at Paul's direction
  on 2026-11-03).
- **Knowledge base:** resources/README.md holds the curated library (10
  resources — six seeded by Paul, four added by his agent) and
  learning-path.md arranges them into Stages 0–4 for future readers.
- The repository is private; all content is written public-safe so it can
  be shared later without a rewrite.
- **Maintenance experiment (2026-10-30):** agents may merge pull requests
  in this repository — see the merge policy in AGENTS.md.

## Next candidates

- The basics queue runs What is an IDE? next. Behind it, the next
  journey article in the weekly queue is Article 008 — From Records to
  Workboards (Series 2), queued at Paul's direction on 2026-11-06; the
  story behind it is already on record at the level of method. The
  weekly working session for this repository is live (Tuesdays, approved
  by Paul on 2026-10-30); its runs have shipped What is an embedding?,
  What is AI infrastructure?, and What is inference?
- Article 002 — Giving the Agent a Memory It Can Keep (the Personal
  Context OS story). Awaits Paul's go-ahead and his review of the draft.
- Articles 003–006 in outline (see the design record in index.json's
  planned list).

## Session log

- **2026-10-30** — Repository designed (v3: human-friendly + AI-native)
  and seeded. Frame, Article 001, glossary (12 terms), patterns (6),
  skills shelf, and this file committed at Paul's direction.
- **2026-10-30** — Paul granted agents PR-merging permission for this
  repository only (an experiment). First exercise: the pull request that
  recorded the policy in AGENTS.md, opened and merged by the agent.
- **2026-10-30** — Paul set the content boundary: journey record, general
  rules, and shareable skills only — no personal information, no project
  specifics. Recorded as the Scope section in AGENTS.md (PR #2).
- **2026-10-30** — Basics batch 2 written at Paul's direction: context
  window, RAG, and agent loop complete the planned concept set, wired
  into the glossary, basics index, and learning path (Stages 1, 2, 4);
  embedding and an infrastructure cluster (AI infrastructure, inference)
  queued as the next planned basics (PR #6).
- **2026-10-30** — Basics gained a tools track at Paul's direction:
  What is GitHub? and What is Obsidian?, wired into the glossary,
  learning path (Stages 1 and 4), and index (PR #5).
- **2026-10-30** — Basics batch 1 written at Paul's direction: five
  concept articles (LLM, token, CLI, API, MCP) in a new basics/ layer,
  with a basics template, glossary entries, and links wired from the
  learning path and front door (PR #4).
- **2026-10-30** — Knowledge base added at Paul's direction: the resources
  library (his six repositories plus four agent-chosen additions, each
  verified live and annotated) and a five-stage learning path for future
  users (PR #3).

- **2026-10-30** — Weekly working session, first run: What is an
  embedding? written (basics, Stage 4, concepts track), wired into the
  glossary, basics index, and learning path (Stage 4); the RAG article's
  "Planned" note for embedding updated to a live link; index.json moved
  embedding from planned_basics to basics; the stale "weekly cadence
  awaits go-ahead" line corrected to record Paul's 2026-10-30 approval
  and the live Tuesday session.

- **2026-10-30** — Weekly working session: What is AI infrastructure?
  written (basics, Stage 4, concepts track), wired into the glossary,
  basics index, and learning path (Stage 4); index.json moved AI
  infrastructure from planned_basics to basics; inference remains as
  the last planned basic.

- **2026-11-03** — Article 007, Onboarding Someone Else (Series 1),
  written at Paul's direction from the week's real work: helping a
  second person start a Personal Context OS, onboard their own
  personal agent, set up a coding agent, and record a first skill
  (a sermon-clip workflow). Published out of order — Articles
  002–006 remain planned — and the queue is unchanged: inference
  is still the last planned basic. Glossary gained Coding agent;
  Patterns 1, 4, and 5 are now also proved by Article 007.
- **2026-11-03** — What is an IDE? queued as a planned basic (tools
  track) at Paul's direction, behind inference in planned_basics.
  Nothing written yet; the weekly session ships it after inference.
- **2026-11-06** — Article 008, From Records to Workboards (Series 2),
  queued as a planned article at Paul's direction, behind inference
  and What is an IDE? in the weekly queue. Queue-only change: no
  article written, nothing else moved.
- **2026-11-10** — Weekly working session: What is inference?
  written (basics, Stage 4, concepts track), wired into the
  glossary, basics index, and learning path (Stage 4); the AI
  infrastructure article's "Planned" note for inference updated to
  a live link; index.json moved inference from planned_basics to
  basics; What is an IDE? remains as the last planned basic.

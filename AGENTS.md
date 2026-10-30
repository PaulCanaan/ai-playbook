# AGENTS.md — instructions for AI agents maintaining this repository

This repository is AI-native: it is written for human readers and maintained
by AI agents working for its owner, Paul. If you are an agent, read this file
first.

## Read order

1. **AGENTS.md** (this file) — the rules.
2. **STATE.md** — where things stand right now.
3. **index.json** — the canonical inventory of every series, article, and
   skill. If it is not in index.json, it does not officially exist yet.

## What this repository is

A running record of one person's AI journey, written to help other people use
AI for their own projects: experience first, in plain language, top-down.
Articles are the journey; patterns.md holds the distilled principles;
glossary.md defines every term; skills/ will hold publishable skills.

## Rules

- **English** for filenames, headings, and canonical terms. Preserve
  source-language quotations when fidelity requires it.
- **Privacy line:** write every article as if it were already public. Never
  include exact residence, family identities, or pastoral/people data.
- **Article numbers are permanent.** Never renumber or reuse a number.
  Articles are cited by number everywhere; index.json maps number to path.
- **Front matter is required** in every article (see
  templates/article-template.md). Keep it accurate when an article changes.
- **index.json is canonical.** Any commit that adds, moves, renames, or
  changes an article, series, or skill updates index.json in the same commit.
  The README table of contents is generated from index.json — update it in
  the same commit too; never let the two drift.
- **STATE.md is updated at the end of every working session**, in the same
  commit as the work it describes when practical.
- **One article (or one fix) per commit.** Commit messages say what changed
  and cite the article number when one is touched.
- **The owner approves changes.** Direct commits and pushes to `main` need
  Paul's explicit go-ahead. Never commit secrets or personal information.
  Pull requests follow the merge policy below — its one scoped exception.

## Pull requests and merging (owner-granted experiment, 2026-10-30)

- Agents working in this repository may open pull requests for proposed
  changes.
- The maintaining agent may **merge** pull requests in **this repository
  only**, after the consistency checks above pass and the pull request
  description states what changed and why. Paul granted this on
  2026-10-30 as an experiment in agent-managed maintenance.
- The permission is scoped to `ai-playbook`. It does **not** extend to any
  other repository, where the owner's per-change review and explicit
  merge instruction remain required.
- Paul may revoke it at any time; a revocation is recorded here and in
  STATE.md.
- **Minimum viable complexity.** Do not add folders, files, or process that
  the current content has not earned.

## Consistency checks — run before calling work done

1. index.json matches the files on disk (paths, titles, statuses).
2. Every internal link resolves to a real file.
3. Every article has complete front matter.
4. Every term an article lists in its front matter exists in glossary.md.
5. Every pattern an article claims is recorded in patterns.md, linked back.
6. STATE.md reflects the new state of the repository.

## Where things live

| Thing | Place |
| --- | --- |
| Articles | `articles/series-N-<slug>/<NNN>-<slug>.md` |
| Skills | `skills/<skill-name>/` (SKILL.md + README.md) |
| Templates | `templates/` |
| Principles | `patterns.md` |
| Terms | `glossary.md` |

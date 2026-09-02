# AI Software Team — Agent Instructions

This repository is the shared control center for an AI-assisted software team.

## Roles
- **ChatGPT / Orchestrator**: product manager, task decomposer, architect, and final reviewer.
- **Codex / Implementer**: implements assigned engineering tasks, runs checks, and reports results.
- **QA / Reviewer**: validates acceptance criteria, regressions, scope, and test coverage.

## Source of Truth
- `PROJECT.md` — product goals, scope, and priorities.
- `ARCHITECTURE.md` — system architecture and technical decisions.
- `TASKS.md` — task queue and current execution state.
- `docs/` — deeper product and engineering knowledge.
- GitHub Issues / Pull Requests — task handoff, implementation status, and review history.

Read the relevant source-of-truth documents before starting work. Do not invent requirements that are not documented or explicitly requested.

## Working Rules
1. Keep changes scoped to the assigned task.
2. Prefer small, reviewable changes and descriptive commits.
3. Do not refactor unrelated code.
4. Add or update tests when behavior changes.
5. Never commit secrets, credentials, API keys, personal data, or local environment files.
6. Before declaring a task complete, run the relevant checks and report the exact commands and results.
7. If requirements conflict or are ambiguous, stop and report the ambiguity instead of guessing.
8. Preserve existing behavior unless the task explicitly requires changing it.

## Task Contract
Every implementation task should define:
- Goal
- Context
- Scope
- Acceptance criteria
- Constraints / non-goals
- Verification steps

## Completion Report
Every completed task should report:
- What changed
- Files changed
- Tests/checks run
- Result
- Remaining risks or follow-up work

## Git / PR Rules
- Use a dedicated branch for non-trivial implementation work when the execution environment supports branches/worktrees.
- Keep commits focused and descriptive.
- Do not merge your own work unless explicitly instructed.
- PRs should explain the problem, solution, verification, and known limitations.

## Context Discipline
Keep this file short. Put detailed, changing knowledge in `docs/` and link to it from the relevant source-of-truth document. This follows the practical Codex pattern of treating `AGENTS.md` as a map rather than an encyclopedia.

# PROJECT — AI Software Team

## Project Mission

Build software through a coordinated AI-agent workflow in which the human provides product intent, ChatGPT decomposes and supervises the work, Codex implements engineering tasks, and GitHub records the shared state.

## Operating Model

Human → ChatGPT Orchestrator → Task Queue → Codex Agent → GitHub → Review → Done / Rework

## Responsibilities

### Human
- Defines business goals and approves important product decisions.
- Provides final approval for releases and irreversible changes.

### ChatGPT / Orchestrator
- Clarifies requirements when necessary.
- Converts product requests into implementation-ready tasks.
- Maintains priorities and dependencies.
- Designs architecture and interfaces.
- Reviews Codex output against acceptance criteria.
- Decides whether work passes, needs rework, or should be split further.

### Codex
- Implements assigned tasks.
- Works within repository instructions.
- Runs relevant tests and checks.
- Reports changed files, verification, and risks.

### QA / Review
- Validates behavior and acceptance criteria.
- Checks regressions, edge cases, security, and scope.

## Task Lifecycle

`BACKLOG → READY → DOING → REVIEW → DONE`

If review fails:

`REVIEW → REWORK → DOING`

## Definition of Done

A task is DONE only when:
1. Acceptance criteria are satisfied.
2. Relevant tests/checks pass.
3. The change is documented when necessary.
4. Scope is limited to the task.
5. Review has passed.
6. Remaining risks are explicitly recorded.

## Current State

This repository is currently the bootstrap/control-center repository. Product-specific application requirements will be added as the first real software project is defined.

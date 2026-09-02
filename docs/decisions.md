# Architecture & Product Decisions

Record decisions that affect multiple tasks or are expensive to reverse.

## Decision Log

### 2026-09-03 — Establish GitHub as the coordination source of truth

**Decision:** Use repository documentation, GitHub Issues, and Pull Requests as the durable handoff protocol between the human, ChatGPT, and Codex agents.

**Reason:** Shared durable state reduces context loss between agents and makes implementation/review traceable.

**Status:** Accepted.

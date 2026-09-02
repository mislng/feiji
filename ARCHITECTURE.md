# ARCHITECTURE

## Current Architecture

The repository currently acts as the control plane for an AI-assisted software team. Application architecture will be documented here once the first product is defined.

## Coordination Architecture

```text
Human
  ↓
ChatGPT Orchestrator
  ├─ Requirements
  ├─ Task decomposition
  ├─ Architecture decisions
  └─ Review
       ↓
GitHub Issues / TASKS.md
       ↓
Codex Agent
       ├─ Implement
       ├─ Test
       └─ Report
       ↓
GitHub commit / PR
       ↓
Review
  ├─ PASS → DONE
  └─ FAIL → REWORK
```

## Design Principles

- GitHub is the shared source of truth for durable task and code state.
- Tasks should be independently executable whenever practical.
- Interfaces and acceptance criteria are defined before implementation.
- Agents should receive enough context to act without loading an unnecessarily large instruction manual.
- Verification is part of implementation, not an optional final step.

## Future Evolution

The workflow may later add automated task dispatch, CI-driven verification, agent specialization, and background orchestration. Such automation should be introduced only after the manual workflow is stable.

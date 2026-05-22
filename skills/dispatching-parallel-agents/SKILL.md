---
name: dispatching-parallel-agents
description: "Use when: multiple independent coding, debugging, or research tasks can be investigated in parallel."
---

Goal: split independent work into isolated agent investigations without losing coordination.

Use for:
- unrelated failing tests across subsystems
- several candidate root causes that do not share state
- broad codebase research where results can be merged later
- independent issue slices after a plan is approved

Do not use for:
- one bug with shared root cause
- tasks that edit the same files concurrently
- work requiring a single global design decision

Workflow:
1. Group tasks by independent problem domain.
2. Write each subtask with exact scope, files, commands, and output format.
3. Give each agent only the context it needs.
4. Ask for evidence, not just conclusions.
5. Merge results, resolve conflicts, and choose next action.

Output:
- task split: domain | reason independent | assigned prompt
- returned findings: evidence | recommendation | risk
- integration decision

Rules:
- one agent per independent domain
- never let agents edit the same file in parallel
- keep main session responsible for final integration

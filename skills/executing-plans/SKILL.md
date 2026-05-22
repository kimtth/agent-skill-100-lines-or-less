---
name: executing-plans
description: "Use when: execute a written implementation plan with checkpoints, verification, and blocker handling."
---

Goal: turn an approved plan into completed, verified work.

Use for:
- plan files with ordered implementation steps
- coding sessions where scope is already agreed
- carrying work through tests, fixes, and final report

Workflow:
1. Load the plan and read it critically before editing.
2. Raise gaps, contradictions, or unsafe steps before starting.
3. Convert plan steps into a live task list.
4. Execute one task at a time and mark status as it changes.
5. Run the verification specified by the plan; add targeted checks if missing.
6. Stop on blockers instead of guessing through unclear instructions.
7. Finish with tests, diff summary, and remaining risk.

Stop when:
- a dependency is missing
- verification fails repeatedly
- instructions conflict with repo reality
- scope expands beyond the approved plan

Rules:
- do not skip plan review
- do not claim completion without fresh evidence
- keep edits scoped to the plan
- ask only when a blocker cannot be resolved locally

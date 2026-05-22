---
name: refactor
description: "Use when: improve code structure, readability, type safety, or maintainability without changing external behavior."
---

Goal: make code easier to change while preserving behavior.

Use for:
- long functions, duplicated logic, unclear names, weak types, or tangled modules
- extracting functions or deep modules
- replacing brittle conditionals with clearer structure
- gradual cleanup before or after a feature

Workflow:
1. Identify the behavior that must not change.
2. Find or add focused tests before risky edits.
3. Make one small refactor at a time.
4. Run targeted verification after each meaningful step.
5. Stop if behavior changes or tests become unclear.
6. Summarize the structural improvement and evidence.

Common moves:
- extract function or object
- rename for domain clarity
- remove duplication
- split orchestration from pure logic
- tighten types and invariants
- isolate side effects

Rules:
- do not mix refactor with feature work
- do not rewrite from scratch unless explicitly requested
- preserve public APIs unless deprecation is part of the plan
- if tests are absent, reduce scope and verify by behavior

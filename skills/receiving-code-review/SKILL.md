---
name: receiving-code-review
description: "Use when: handling code review feedback before implementing suggestions or pushing back."
---

Goal: respond to review feedback with technical rigor, not automatic agreement.

Workflow:
1. Read every review item before editing.
2. Restate the technical requirement when it is unclear.
3. Verify each claim against code, tests, docs, and runtime behavior.
4. Decide whether the feedback is correct for this codebase.
5. Implement one item at a time with focused verification.
6. Push back with evidence when a suggestion is wrong or risky.

Use for:
- PR review comments
- reviewer requests that appear contradictory
- broad requests such as "fix 1-6"
- feedback that changes API, behavior, or test expectations

Response pattern:
- understood requirement
- evidence checked
- action taken or reasoned pushback
- verification result

Rules:
- do not say feedback is right before checking
- do not implement unclear items silently
- avoid bundling unrelated review fixes
- keep behavior changes explicit

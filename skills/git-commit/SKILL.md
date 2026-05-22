---
name: git-commit
description: "Use when: create a conventional git commit from the current diff with logical staging and message analysis."
---

Goal: create one clear commit that matches the actual change.

Use for:
- "commit this", "write a commit message", or `/commit`
- grouping related file changes
- generating Conventional Commit messages from a diff

Workflow:
1. Inspect `git status --short` and the relevant diff.
2. Separate unrelated user changes from this task's changes.
3. Stage only the intended logical group.
4. Choose type and optional scope from the diff.
5. Write an imperative subject under 72 chars, ideally under 50.
6. Add a body only when the reason is not obvious.
7. Commit only after explicit user approval.

Types:
- feat, fix, refactor, perf, docs, test, chore, build, ci, style, revert

Message shape:
```text
<type>(<scope>): <imperative summary>

<body only when useful>
```

Rules:
- do not stage unrelated changes
- do not include secrets or generated noise
- do not commit without the user's clear request
- mention tests or verification in the body only when relevant

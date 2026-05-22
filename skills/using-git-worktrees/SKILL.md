---
name: using-git-worktrees
description: "Use when: starting feature work that should be isolated from the current checkout or branch."
---

Goal: create or detect an isolated workspace without fighting the user's tooling.

Workflow:
1. Detect whether the repo is already in a worktree.
2. Guard against mistaking submodules for worktrees.
3. Ask before creating a new worktree unless instructions already allow it.
4. Prefer platform-native worktree tools when available.
5. Fall back to `git worktree add` only when no native tool exists.
6. Run project setup in the isolated workspace.
7. Record branch, path, and cleanup expectations.

Checks:
```bash
git rev-parse --git-dir
git rev-parse --git-common-dir
git branch --show-current
git rev-parse --show-superproject-working-tree
```

Use for:
- risky feature work
- parallel implementation branches
- executing plans while preserving the user's current checkout

Rules:
- do not create nested or duplicate worktrees
- do not switch the user's current branch as a shortcut
- do not delete a worktree until changes are integrated or abandoned by request
- explain detached HEAD limitations before finishing

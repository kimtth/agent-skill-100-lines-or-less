---
name: finishing-a-development-branch
description: "Use when: implementation is complete and you need to verify, summarize, and choose merge, PR, commit, or cleanup flow."
---

Goal: finish development work without losing verification or branch hygiene.

Workflow:
1. Run the project's relevant tests before presenting completion options.
2. Inspect git status, branch, worktree state, and uncommitted changes.
3. Summarize what changed and what evidence passed.
4. Present integration options: commit, open PR, merge, leave changes, or cleanup.
5. Execute only the user's chosen option.
6. Clean temporary branches/worktrees only when safe and approved.

If tests fail:
- show the failing command and failure count
- stop integration work
- fix or ask before proceeding

Git checks:
- `git status --short`
- current branch
- worktree vs normal checkout
- staged vs unstaged changes

Rules:
- do not merge, commit, or delete branches without explicit approval
- do not present PR/merge as ready until verification passes
- keep unrelated dirty work separate
- include residual risk in the final handoff

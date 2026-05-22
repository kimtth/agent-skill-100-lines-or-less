---
name: skills-cli
description: "Use when: discover, install, list, check, update, remove, back up, restore, sync, or initialize Agent Skills with bunx/npx skills."
---

Goal: manage Agent Skills from the CLI without guessing syntax.

Use for:
- `bunx skills`, `npx skills`, `skills.sh`, or `skills-lock.json`
- finding skills, installing one skill from a repo, or syncing agent targets
- backing up, restoring, updating, removing, or initializing skill packages

Current syntax:
- search: `bunx skills find <query>`
- install repo skill: `bunx skills add <source> --skill <name>`
- install direct path: `bunx skills add https://github.com/org/repo/tree/main/skills/name`
- inspect: `bunx skills list`, `bunx skills check`
- maintain: `bunx skills update`, `bunx skills remove <name>`
- start package: `bunx skills init`

Workflow:
1. Identify the target agent and install scope.
2. Prefer `bunx`; use `npx` when Bun is unavailable.
3. Use skills.sh for discovery, then verify source and repo health.
4. Install only after the user agrees.
5. Re-run `list` or `check` to confirm the result.

Quality checks:
- prefer official or source-author skills
- inspect low-install or unknown repos before recommending
- avoid old `owner/repo@skill` syntax

Rules:
- show the exact command and one expected confirmation
- keep CLI branches short and executable
- say what is unknown instead of adding flags by habit
- do not mutate user/global skill state without consent
- do not paste secrets from lockfiles or environment output
- when a command fails, report the exact command and error

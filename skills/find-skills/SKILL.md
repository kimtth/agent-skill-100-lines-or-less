---
name: find-skills
description: "Use when: find, compare, install, update, or remove agent skills from skills.sh or a source repo."
---

Goal: help the user add the smallest trustworthy skill that solves the task.

Use for:
- "find a skill for X", "is there a skill that can X", or "how do I do X"
- browsing skills.sh, comparing candidates, or checking install commands
- managing installed skills with `bunx skills` or `npx skills`

Workflow:
1. Restate the capability needed: domain, task, and target agent.
2. Check local skills first so you do not recommend duplicates.
3. Search skills.sh or run `bunx skills find <query>` when needed.
4. Verify source reputation, install count, repo health, and fit.
5. Present up to 3 options, then one recommended default.

Install commands:
- `bunx skills find <query>`
- `bunx skills add <source> --skill <name>`
- `bunx skills list`, `check`, `update`, `remove <name>`

Output:
- candidates: name | source | why it fits | caveat
- recommendation: skill | install command | confidence
- no-match: what was searched | useful fallback

Rules:
- keep the evidence next to the recommendation
- prefer one good command over a tour of the ecosystem
- say "no good match" when the catalog is weak
- do not install or overwrite agent config without consent
- prefer official, maintained, audited, or source-author skills
- call out stale, duplicate, or low-install results

---
name: write-a-skill
description: "Use when: create or improve an agent skill with proper frontmatter, structure, triggers, and progressive disclosure."
---

Goal: create skills that load only when useful and stay easy to inspect.

Use for:
- new `SKILL.md` files
- refactoring bulky skills into compact workflows
- fixing discovery descriptions or folder/name mismatches
- deciding when references or scripts are justified

Workflow:
1. Define the task, trigger phrases, target user, and expected output.
2. Choose whether the skill is instructions-only or needs bundled assets.
3. Create `skills/<name>/SKILL.md` with matching frontmatter `name`.
4. Put trigger language in `description`; quote descriptions with colons.
5. Keep the main file concise; move long reference material only when needed.
6. Validate frontmatter, folder name, line count, and actual invocation fit.

Structure:
- goal
- use for
- workflow
- output
- rules

Rules:
- do not create a skill when a short prompt or README note is enough
- scripts are for deterministic repeatable work, not decoration
- keep public examples executable and minimal
- avoid broad always-on wording in descriptions

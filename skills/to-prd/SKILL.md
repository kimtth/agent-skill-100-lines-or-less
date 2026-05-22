---
name: to-prd
description: "Use when: turn current conversation and repo context into a PRD for an issue tracker."
---

Goal: produce a practical PRD from what is already known.

Use for:
- converting a feature discussion into a product requirements document
- capturing user stories, implementation decisions, and testable scope
- preparing work for issue tracking or agent handoff

Workflow:
1. Read existing conversation, repo shape, glossary, ADRs, and relevant code.
2. Do not interview from scratch; ask only for missing blockers.
3. Identify modules to build or modify, preferring deep testable interfaces.
4. Write user stories, implementation decisions, acceptance criteria, and risks.
5. Include test expectations and open questions.
6. Publish or prepare for the issue tracker only when target labels are known.

PRD sections:
- problem statement
- solution
- user stories
- implementation decisions
- acceptance criteria
- test plan
- risks and open questions

Rules:
- use the project vocabulary, not generic product prose
- keep scope traceable to user-visible outcomes
- separate known decisions from assumptions
- prefer small modules that can be tested in isolation

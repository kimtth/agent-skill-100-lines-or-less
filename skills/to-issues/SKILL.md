---
name: to-issues
description: "Use when: break a plan, spec, or PRD into independently grabbable implementation issues."
---

Goal: turn a plan into thin vertical slices an agent or developer can finish.

Use for:
- converting PRDs, plans, or issue threads into implementation tickets
- splitting large features into demoable end-to-end slices
- marking work as human-in-the-loop or agent-ready

Workflow:
1. Read the source plan, PRD, issue, and comments.
2. Explore the codebase only as needed to use correct module names.
3. Draft tracer-bullet slices that cut through schema, API, UI, and tests.
4. Mark each issue as AFK or HITL and list blockers.
5. Ask the user to approve granularity before publishing.
6. Create issues with clear verification steps and labels.

Issue template:
- title
- user story or source requirement
- scope
- implementation notes
- verification
- blocked by
- AFK/HITL

Rules:
- prefer many small complete slices over one horizontal layer task
- each issue must be independently verifiable
- do not hide dependency order
- use the repo's domain vocabulary

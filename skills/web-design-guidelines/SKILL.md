---
name: web-design-guidelines
description: "Use when: review UI code, audit accessibility, check UX, or compare a site against current Web Interface Guidelines."
metadata:
	author: vercel
	version: "1.0.0"
	argument-hint: <file-or-pattern>
---

Goal: review real UI files against the latest web interface rules.

Workflow:
1. Fetch fresh guidelines from:
	 `https://raw.githubusercontent.com/vercel-labs/web-interface-guidelines/main/command.md`
2. Read the user-provided file or glob. If none is provided, ask for scope.
3. Check layout, accessibility, copy, responsive behavior, and interaction polish.
4. Report findings in the terse format required by the fetched guidelines.

Use for:
- "review my UI", "audit this design", "check accessibility"
- landing pages, apps, dashboards, forms, and component previews
- visual issues that need file-backed evidence, not taste alone

Output:
- findings first: file:line | rule | issue | fix
- note only the highest-signal passes when there are no findings
- mention when guidelines could not be fetched

Rules:
- tie each critique to a visible user outcome
- prefer concrete file edits over design vocabulary
- remove weak UI before adding ornament
- fetch the guideline source before each review
- do not invent rules that are not in the fetched document
- ask for target files when scope is missing

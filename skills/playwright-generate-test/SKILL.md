---
name: playwright-generate-test
description: "Use when: generate a Playwright test from a user scenario by first exploring the UI and then saving a passing test."
---

Goal: generate a Playwright test from observed UI behavior.

Workflow:
1. Ask for a scenario if missing.
2. Open or run the app and walk the flow with browser or Playwright tools.
3. Capture stable role, label, or text locators.
4. Save a TypeScript test under the project's tests folder.
5. Run it and iterate until pass or report the blocker.

Rules:
- assert user-visible outcomes, not implementation details
- avoid arbitrary sleeps and brittle CSS
- report file path, command, and result

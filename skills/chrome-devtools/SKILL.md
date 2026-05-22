---
name: chrome-devtools
description: "Use when: debug, inspect, automate, screenshot, profile, or analyze a web page with Chrome DevTools-style browser tools."
---

Goal: debug rendered browser behavior with evidence from the page.

Use for:
- console errors, network failures, layout bugs, and interaction issues
- screenshots or accessibility tree inspection
- JavaScript evaluation in page context
- performance profiling and Core Web Vital investigation
- viewport, CPU, network, or geolocation emulation

Workflow:
1. Open or select the target page.
2. Capture page state before interacting.
3. Use accessible snapshots to find stable targets.
4. Reproduce the issue with clicks, inputs, navigation, or scripts.
5. Inspect console, network, DOM state, and screenshots.
6. Apply the smallest code fix and re-check the page.

Evidence to collect:
- URL and viewport
- screenshot or snapshot
- console message or stack
- failed request and status
- timing or performance trace when relevant

Rules:
- prefer observed page state over static guesses
- do not rely on fragile coordinates when selectors are available
- preserve logged-in or user session context when needed
- verify the rendered fix, not just the source diff

---
name: verification-before-completion
description: "Use when: about to claim work is complete, fixed, passing, or ready for commit or PR."
---

Goal: make completion claims only after fresh evidence.

Gate:
1. Identify the exact claim being made.
2. Choose the command or inspection that proves it.
3. Run the full check now, not from memory.
4. Read output and exit code.
5. State the result with evidence or report the actual failure.

Examples:
- tests pass: test command exits 0 with failure count checked
- build succeeds: build command exits 0
- bug fixed: original symptom is reproduced as passing
- lint clean: linter output has no errors
- requirements met: checklist is matched against the request

Red flags:
- "should pass"
- "looks good"
- "probably fixed"
- claiming success after partial output
- relying on an earlier run after new edits

Output:
- command run
- result
- evidence summary
- residual risk or skipped checks

Rules:
- no completion claim without current verification
- do not summarize success before reading output
- if verification cannot run, say why and what risk remains

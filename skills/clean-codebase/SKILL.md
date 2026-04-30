---
name: clean-codebase
description: Clean up dead code, obsolete paths, and contradictions in the codebase to keep it small, correct, and aligned with reality.
---

Goal: keep repo small, correct, aligned with reality

Tasks:
1. Delete dead code (no refs, no tests, stale)
2. Remove obsolete paths, flags, duplicates
3. Sync docs with actual APIs/configs
4. Detect contradictions:
   - code vs docs
   - code vs tests
   - schema/type drift
   - unreachable logic

Output:
- list of removals (with confidence)
- suggested diffs
- contradictions:
  type | where | issue | severity | fix

Mode: assist (auto-fix safe only)
Rules:
- don’t remove public APIs without deprecation
- avoid dynamic/reflection false positives
- keep changes reversible

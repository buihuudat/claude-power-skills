# /ship — Ship Feature End-to-End

Turn the following requirement into a complete, production-ready feature:

**Feature:** $ARGUMENTS

---

## Phase 1: Clarify (before writing a single line of code)
1. Define exact scope — what is IN, what is OUT
2. Define verifiable success criteria
3. Identify risks and unknowns
4. If there is ambiguity → ask now, do not guess

## Phase 2: Plan (5 minutes max)
Create a concise checklist of steps, with a verification checkpoint after each major step.
Do not over-plan for things not yet needed.

## Phase 3: Implement (surgical, minimal)
- Write the minimum code required to meet the success criteria
- Do not add "just in case" features
- Do not refactor unrelated code
- Match the existing codebase style
- After each major step: verify the checkpoint

## Phase 4: Test
- Manually verify the happy path
- Manually verify the edge cases identified in Phase 1
- If a test suite exists: run it and ensure it passes
- If no tests exist: write at least 1 test for the most important behavior

## Phase 5: Ship Checklist
- [ ] Code works correctly against the defined success criteria
- [ ] No debug logs, TODOs, or dead code
- [ ] No regressions in related features
- [ ] Clean diff — only what is necessary

---
Final output: a short description of what was done and how to verify it.

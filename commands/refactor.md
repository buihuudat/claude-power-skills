# /refactor — Safe Surgical Refactor

Refactor target: $ARGUMENTS

---

## Rule: Refactor = change structure, NOT behavior.

## Step 1: Define Scope (no scope creep)
- Exactly what needs refactoring and WHY
- Clear boundary: what will change, what will NOT change
- If there is no specific reason → do not refactor

## Step 2: Safety Net
- Do existing tests cover this behavior?
- If not → write characterization tests BEFORE refactoring
- "Behavior unchanged" must be verifiable, not just claimed

## Step 3: Refactor (small steps)
Each step:
1. Make a small change
2. Tests still pass
3. Commit (or checkpoint)
4. Next step

No "big bang" refactoring of everything at once before testing.

## Step 4: Code Quality Check
After refactoring, verify:
- [ ] Behavior is identical to before (tests pass)
- [ ] Code is easier to read (or at least no worse)
- [ ] No new unnecessary abstractions
- [ ] No new dead code

## Step 5: Diff Review
- Is the diff clean? Are there any out-of-scope changes?
- If yes → revert the out-of-scope changes

---
If the refactor leads to "we also need to change X, Y, Z" → stop and split into separate tasks.

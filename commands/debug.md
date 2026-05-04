# /debug — Systematic Debugging

Bug to debug: $ARGUMENTS

---

## Rule: No guessing. Prove everything with evidence.

## Step 1: Reproduce (confirm the bug exists)
- Find a way to reproduce the bug deterministically
- If it cannot be reproduced → it cannot be fixed
- What is the minimal reproduction case?

## Step 2: Observe (collect data)
- Actual behavior: [what is happening]
- Expected behavior: [what should happen]
- When does it occur / not occur?
- Full logs, error messages, stack traces

## Step 3: Hypothesize (form hypotheses)
List 3–5 possible causes, ranked from most to least likely:
1. [Hypothesis A] — supporting evidence: ..., contradicting evidence: ...
2. [Hypothesis B] — ...
3. ...

## Step 4: Test Hypotheses (systematic elimination)
For each hypothesis: design the smallest possible test to confirm or refute it.
Do not fix anything until the root cause is identified.

## Step 5: Fix (surgical)
- Fix the root cause, not the symptom
- Minimal change
- Explain why this fix is correct

## Step 6: Verify + Prevent
- Re-run the reproduction case → bug is gone
- Check for regressions
- Add a test to prevent this bug from recurring

---
Red flags to avoid: "let's try this", "maybe it's", fix-and-pray, changing multiple things at once.

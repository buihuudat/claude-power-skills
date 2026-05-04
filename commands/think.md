# /think — Deep Reasoning Before Action

Before touching any code, reason through this task completely:

**Task:** $ARGUMENTS

---

## Step 1: Understand (no assumptions)
- What is actually being asked? (not what I think is being asked)
- How many different interpretations of this requirement exist?
- Read relevant code, trace data flow, fully understand context before writing a single line

## Step 2: Surface Hidden Complexity
- What looks simple but is actually complicated?
- Which edge cases will definitely appear?
- Which dependencies will be affected?
- Are there race conditions, state mutations, or side effects?

## Step 3: Multiple Approaches
List at least 3 different approaches:
- Approach A: [simplest]
- Approach B: [balanced]
- Approach C: [most powerful but more complex]

For each approach: what are the tradeoffs? When should it be used?

## Step 4: Recommendation
- Which approach do I recommend and WHY specifically for this problem
- What I need confirmed before starting

## Step 5: Success Criteria
Instead of "fix the bug", define success as:
- [ ] Test case X passes
- [ ] Behavior Y works correctly with input Z
- [ ] No regressions in modules A, B

---
Only begin implementation AFTER completing all 5 steps above.

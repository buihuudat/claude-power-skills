# /test — Generate Comprehensive Tests

Write tests for: $ARGUMENTS

---

## Rule: Tests must catch real bugs, not just exist for coverage.

## Step 1: Understand Behavior (read the code first)
- What is the public contract? (inputs → outputs)
- Which side effects need to be verified
- Are error cases documented?

## Step 2: Test Categories

### Happy Path
- Typical use case with normal input
- Verify the output is correct

### Edge Cases (most important)
- Empty/null/undefined inputs
- Boundary values (0, 1, max, max+1)
- Empty collections, single-item collections
- Unicode, special characters (if handling strings)

### Error Cases
- Invalid inputs → are error messages correct?
- External failures (network, DB) → handled gracefully?
- Concurrent access (if relevant)

### Regression Tests
- If fixing a bug: write a test that reproduces the bug FIRST, verify it fails, then fix

## Step 3: Test Quality Check
For each test:
- [ ] Test name describes behavior, not implementation
- [ ] One test tests one thing
- [ ] Clear, unambiguous assertions
- [ ] Test is independent (no dependency on order or global state)
- [ ] Fast (mock external dependencies)

## Step 4: Coverage Assessment
- Which behaviors are still untested?
- Is it worthwhile to test them or is it over-testing?

---
Prioritize testing important behavior over achieving 100% coverage.

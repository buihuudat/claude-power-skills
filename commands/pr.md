# /pr — Create Pull Request

Create a PR for: $ARGUMENTS

---

## Step 1: Review Changes
Before creating the PR, check:
- `git diff main...HEAD` — view all changes
- Are there files that should not be committed? (.env, secrets, debug logs)
- Is the diff clean? Are there any "drive-by" changes?

## Step 2: PR Title
Format: `<type>: <short description>` (under 70 characters)
Types: `feat`, `fix`, `refactor`, `perf`, `test`, `docs`, `chore`

## Step 3: PR Description

### What
- What changed? (facts, no long explanations needed)

### Why
- Why is this change needed? Business context, bug report, performance data

### How (only when the approach is not obvious)
- What important design decisions were made?
- What alternatives were considered and rejected?

### Test Plan
- [ ] Happy path: [specific description]
- [ ] Edge cases: [description]
- [ ] Regression: [what was verified not to be broken]

### Screenshots/Demo (if UI changes)

## Step 4: Self-Review Checklist
- [ ] Code works correctly against the stated goal
- [ ] No new untracked TODOs/FIXMEs
- [ ] No console.log/print debug statements
- [ ] Tests pass
- [ ] Clean diff — only what is necessary

---
Create the PR only after the checklist is complete.

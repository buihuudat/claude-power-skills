# Real-World Examples

Concrete before/after examples showing how each command changes Claude's behavior.

---

## /think — Stop Assuming, Start Clarifying

**Without `/think`:**
```
User: add user export feature
Claude: [immediately writes code to export users as CSV]
```

**With `/think add user export feature`:**
```
Claude:

Step 1 - Multiple interpretations:
  A) Export current user's own data (GDPR compliance)
  B) Admin exports all users (bulk operation)
  C) Export users matching a filter

Step 2 - Hidden complexity:
  - Which fields? (PII implications differ)
  - What format? (CSV vs JSON vs Excel)
  - Async job or synchronous download?
  - Rate limiting needed?

Step 3 - Approaches:
  A) Simple: synchronous CSV, all fields, admin only
  B) Balanced: async job, configurable fields, audit log
  C) Full: streaming export, format options, GDPR-compliant field filtering

Recommendation: Approach A for now unless scale > 10k users
Needs confirmation: who can export? which fields?

Success criteria:
  - [ ] Download triggers correctly
  - [ ] File opens in Excel without errors
  - [ ] PII fields excluded unless explicitly included
```

---

## /debug — Root Cause, Not Symptom Patching

**Without `/debug`:**
```
User: login broken for some users
Claude: [changes password comparison logic, tries bcrypt update, adds logging]
// Bug persists, 3 files changed
```

**With `/debug login fails for users with uppercase emails`:**
```
Claude:

Step 1 - Reproduce:
  Created test: login('TEST@email.com', 'pass') → fails
  login('test@email.com', 'pass') → succeeds ✓ Reproduced.

Step 2 - Observe:
  Error: "User not found" (not "Invalid password")
  → Problem is in lookup, not authentication

Step 3 - Hypotheses (ranked):
  1. [HIGH] Email stored lowercase, lookup is case-sensitive → test: query DB directly
  2. [MED] Email normalized on signup but not on login → test: check signup code
  3. [LOW] DB collation issue → test: check schema

Step 4 - Test hypothesis 1:
  DB query: SELECT * FROM users WHERE email = 'TEST@email.com' → 0 rows
  DB query: SELECT * FROM users WHERE email = 'test@email.com' → 1 row ✓ Confirmed.

Fix: normalize email to lowercase in login handler (1 line)
  auth.ts:47  email = email.toLowerCase()

Prevention: add test for case-insensitive login
```

---

## /audit — Security Issues You'd Miss in Review

**`/audit src/api/payments.ts`:**
```
[CRITICAL] payments.ts:23
> amount passed directly to SQL query — SQL injection vulnerability
> Fix: use parameterized query: db.query('SELECT * FROM orders WHERE amount = ?', [amount])

[HIGH] payments.ts:67
> stripe_secret_key hardcoded in source
> Fix: move to environment variable, rotate key immediately

[HIGH] payments.ts:91
> No authentication check before processing refund
> Fix: verify req.user.role === 'admin' before refund endpoint

[MEDIUM] payments.ts:134
> N+1 query in loop — fetches order details individually for each line item
> Fix: batch fetch with WHERE id IN (...) before loop

[LOW] payments.ts:156
> console.log(cardData) — potential PII in logs
> Fix: remove or redact sensitive fields

Top 3 to fix immediately: SQL injection (23), hardcoded secret (67), missing auth (91)
```

---

## /ship — Feature Done Right

**`/ship add dark mode toggle to settings page`:**
```
Phase 1 - Clarify:
  ✓ Scope: toggle in settings, persist preference, apply globally
  ✓ Success: toggle works, preference survives page refresh, no flash on load
  ✓ Risk: CSS variable conflicts with existing themes

Phase 2 - Plan:
  1. Add CSS variables for light/dark tokens
  2. Store preference in localStorage
  3. Apply class on <html> before paint (prevent flash)
  4. Add toggle component to settings page
  Checkpoint: visual verification after each step

Phase 3 - Implement:
  [implements each step, verifies checkpoint]

Phase 4 - Test:
  ✓ Toggle switches theme
  ✓ Preference persists on refresh
  ✓ No flash of wrong theme on load
  ✓ Existing components unaffected

Phase 5 - Ship Checklist:
  ✓ No debug logs
  ✓ Diff: 4 files, +67 -2 lines (clean)
  ✓ Feature works as specified
```

---

## /refactor — Safe, Not Brave

**Without `/refactor`:**
```
User: refactor UserService
Claude: [rewrites entire service, changes method signatures, 
        adds new abstractions, touches 12 files]
// Half the tests break
```

**With `/refactor UserService — extract email validation logic`:**
```
Step 1 - Scope:
  IN: extract isValidEmail() to shared utils
  OUT: everything else in UserService

Step 2 - Safety net:
  Existing tests cover email validation? → Yes, 3 tests
  Running: ✓ all pass

Step 3 - Steps:
  a) Copy logic to utils/validation.ts → tests still pass ✓
  b) Import in UserService, use new function → tests still pass ✓
  c) Remove old inline code → tests still pass ✓

Step 4 - Diff:
  2 files changed, +8 -6 lines
  Behavior: identical (proven by tests)
```

---

## /perf — Measure, Then Optimize

**`/perf dashboard loads slowly`:**
```
Step 1 - Profile:
  Added timing logs → DB queries: 2.3s, rendering: 0.1s
  Bottleneck is database, not frontend

Step 2 - Analysis:
  dashboard query: O(n) users × O(m) posts = O(n×m) queries
  Found: N+1 pattern — fetching post count per user in loop

Step 3 - Fix (high impact, low effort):
  Before: users.forEach(u => u.postCount = await db.count(u.id))
  After:  const counts = await db.countByUser(userIds) // 1 query

Step 4 - Verify:
  Before: 2.3s (47 queries for 47 users)
  After: 0.08s (2 queries total)
  Behavior: identical output ✓
```

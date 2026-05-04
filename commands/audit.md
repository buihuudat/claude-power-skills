# /audit — Full Code Audit

Perform a comprehensive audit of: $ARGUMENTS

---

## 1. Correctness
- Logic bugs, off-by-one errors, wrong conditionals
- Null/undefined/empty cases not handled
- Type mismatches, dangerous implicit coercions
- Concurrent access issues (race conditions, shared mutable state)

## 2. Security (OWASP Top 10 mindset)
- Injection vulnerabilities (SQL, command, XSS, path traversal)
- Authentication & authorization gaps
- Sensitive data exposure (hardcoded secrets, logging PII)
- Input validation at system boundaries
- Notable dependency vulnerabilities

## 3. Performance
- N+1 queries, unnecessary loops, redundant computation
- Memory leaks, unbounded growth
- Blocking operations in async context
- Missing indexes, inefficient data structures

## 4. Code Quality
- Functions/classes doing more than one thing
- Unearned abstractions (YAGNI violations)
- Dead code, unreachable branches
- Inconsistent naming, style violations

## 5. Reliability
- Missing or incorrect error handling
- Retry logic for external calls
- Timeout handling
- Graceful degradation

---

## Output Format
For each issue found:
**[SEVERITY: CRITICAL/HIGH/MEDIUM/LOW]** `file:line`
> Specific description of the problem
> Suggested fix (code snippet if needed)

End with: the top 3 issues to fix immediately.

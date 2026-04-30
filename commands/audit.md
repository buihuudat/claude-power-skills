# /audit — Full Code Audit

Thực hiện audit toàn diện cho: $ARGUMENTS

---

## 1. Correctness
- Logic bugs, off-by-one errors, wrong conditionals
- Null/undefined/empty cases không được handle
- Type mismatches, implicit coercions nguy hiểm
- Concurrent access issues (race conditions, shared mutable state)

## 2. Security (OWASP Top 10 mindset)
- Injection vulnerabilities (SQL, command, XSS, path traversal)
- Authentication & authorization gaps
- Sensitive data exposure (secrets hardcoded, logging PII)
- Input validation ở system boundaries
- Dependency vulnerabilities nổi bật

## 3. Performance
- N+1 queries, unnecessary loops, redundant computation
- Memory leaks, unbounded growth
- Blocking operations trong async context
- Missing indexes, inefficient data structures

## 4. Code Quality
- Functions/classes làm nhiều hơn một việc
- Abstractions chưa earn được (YAGNI violations)
- Dead code, unreachable branches
- Inconsistent naming, style violations

## 5. Reliability
- Error handling thiếu hoặc sai
- Retry logic cho external calls
- Timeout handling
- Graceful degradation

---

## Output Format
Với mỗi issue tìm được:
**[SEVERITY: CRITICAL/HIGH/MEDIUM/LOW]** `file:line`
> Mô tả vấn đề cụ thể
> Suggested fix (code snippet nếu cần)

Kết thúc bằng: top 3 issues cần fix ngay nhất.

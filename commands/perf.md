# /perf — Performance Analysis & Optimization

Analyze performance cho: $ARGUMENTS

---

## Nguyên tắc: Measure first. Optimize second. Never guess.

## Step 1: Profile (không optimize mù)
- Bottleneck thực sự ở đâu? (không phải ở đâu ta nghĩ)
- Có benchmark/profiling data không?
- Nếu không → cách measure performance hiện tại là gì?

## Step 2: Complexity Analysis
- Time complexity: O(?) với input size n
- Space complexity: O(?)
- Worst case vs average case vs best case
- Hidden constants (cache misses, system calls, allocations)

## Step 3: Common Bottlenecks (kiểm tra theo thứ tự)
**Database/IO (thường là vấn đề #1)**
- N+1 queries
- Missing indexes
- Fetching quá nhiều data (SELECT *)
- Không dùng connection pooling

**Algorithm**
- O(n²) loops có thể thành O(n log n) hoặc O(n)
- Redundant computation (memoize/cache được không?)
- Wrong data structure cho use case

**Memory**
- Unnecessary allocations trong hot path
- Memory leaks
- Large objects không cần thiết

**Concurrency**
- Sequential operations có thể parallel
- Lock contention
- Blocking I/O trong async context

## Step 4: Optimization Plan
Sắp xếp theo impact/effort ratio:
1. [High impact, low effort] → làm ngay
2. [High impact, high effort] → plan carefully
3. [Low impact, *] → probably skip

## Step 5: Verify Improvement
- Benchmark trước và sau
- Không regression ở correctness
- Document tradeoffs (readability, maintainability)

---
"Premature optimization is the root of all evil" — nhưng "known bottleneck" thì phải fix.

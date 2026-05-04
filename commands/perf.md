# /perf — Performance Analysis & Optimization

Analyze performance for: $ARGUMENTS

---

## Rule: Measure first. Optimize second. Never guess.

## Step 1: Profile (do not optimize blind)
- Where is the actual bottleneck? (not where we think it is)
- Is there existing benchmark/profiling data?
- If not → how do we measure current performance?

## Step 2: Complexity Analysis
- Time complexity: O(?) with input size n
- Space complexity: O(?)
- Worst case vs average case vs best case
- Hidden constants (cache misses, system calls, allocations)

## Step 3: Common Bottlenecks (check in this order)
**Database/IO (usually problem #1)**
- N+1 queries
- Missing indexes
- Fetching too much data (SELECT *)
- Not using connection pooling

**Algorithm**
- O(n²) loops that could be O(n log n) or O(n)
- Redundant computation (can it be memoized/cached?)
- Wrong data structure for the use case

**Memory**
- Unnecessary allocations in the hot path
- Memory leaks
- Large objects that are not needed

**Concurrency**
- Sequential operations that could be parallel
- Lock contention
- Blocking I/O in async context

## Step 4: Optimization Plan
Rank by impact/effort ratio:
1. [High impact, low effort] → do immediately
2. [High impact, high effort] → plan carefully
3. [Low impact, *] → probably skip

## Step 5: Verify Improvement
- Benchmark before and after
- No regressions in correctness
- Document tradeoffs (readability, maintainability)

---
"Premature optimization is the root of all evil" — but a known bottleneck must be fixed.

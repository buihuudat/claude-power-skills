# /test — Generate Comprehensive Tests

Viết tests cho: $ARGUMENTS

---

## Nguyên tắc: Tests phải catch real bugs, không phải chỉ để coverage.

## Step 1: Understand Behavior (đọc code trước)
- Public contract là gì? (inputs → outputs)
- Side effects cần verify
- Error cases được document không?

## Step 2: Test Categories

### Happy Path
- Typical use case với input bình thường
- Verify output chính xác

### Edge Cases (quan trọng nhất)
- Empty/null/undefined inputs
- Boundary values (0, 1, max, max+1)
- Empty collections, single-item collections
- Unicode, special characters (nếu xử lý strings)

### Error Cases
- Invalid inputs → error messages đúng không?
- External failures (network, DB) → handle gracefully không?
- Concurrent access (nếu relevant)

### Regression Tests
- Nếu đang fix bug: viết test reproduce bug TRƯỚC, verify nó fail, rồi fix

## Step 3: Test Quality Check
Với mỗi test:
- [ ] Tên test mô tả behavior, không mô tả implementation
- [ ] Một test chỉ test một thing
- [ ] Assert rõ ràng, không ambiguous
- [ ] Test độc lập (không phụ thuộc order, global state)
- [ ] Nhanh (mock external dependencies)

## Step 4: Coverage Assessment
- Những behavior nào vẫn chưa được test?
- Có worthwhile để test không hay over-testing?

---
Ưu tiên test behavior quan trọng > đạt 100% coverage.

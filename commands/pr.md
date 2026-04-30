# /pr — Create Pull Request

Tạo PR cho: $ARGUMENTS

---

## Step 1: Review Changes
Trước khi tạo PR, kiểm tra:
- `git diff main...HEAD` — xem toàn bộ changes
- Có file nào không nên commit không? (.env, secrets, debug logs)
- Diff có gọn không? Có "drive-by" changes không?

## Step 2: PR Title
Format: `<type>: <mô tả ngắn gọn>` (dưới 70 ký tự)
Types: `feat`, `fix`, `refactor`, `perf`, `test`, `docs`, `chore`

## Step 3: PR Description

### What
- Thay đổi gì? (facts, không cần giải thích dài)

### Why  
- Tại sao cần thay đổi này? Business context, bug report, performance data

### How (chỉ khi approach không obvious)
- Quyết định design quan trọng nào?
- Alternatives nào đã được cân nhắc và loại bỏ?

### Test Plan
- [ ] Happy path: [mô tả cụ thể]
- [ ] Edge cases: [mô tả]
- [ ] Regression: [gì đã được verify không bị break]

### Screenshots/Demo (nếu UI changes)

## Step 4: Self-Review Checklist
- [ ] Code hoạt động đúng với mục tiêu đã định
- [ ] Không có TODO/FIXME mới chưa được track
- [ ] Không có console.log/print debug
- [ ] Tests pass
- [ ] Diff sạch — chỉ những gì cần thiết

---
Tạo PR sau khi checklist hoàn chỉnh.

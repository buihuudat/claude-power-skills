# /ship — Ship Feature End-to-End

Biến yêu cầu sau thành feature hoàn chỉnh, production-ready:

**Feature:** $ARGUMENTS

---

## Phase 1: Clarify (trước khi viết bất kỳ dòng code nào)
1. Xác định scope chính xác — cái gì IN, cái gì OUT
2. Xác định success criteria có thể verify được
3. Xác định rủi ro và unknowns
4. Nếu có ambiguity → hỏi ngay, không đoán

## Phase 2: Plan (tối đa 5 phút)
Tạo checklist ngắn gọn các bước cần làm, với verification checkpoint sau mỗi bước lớn.
Không lập kế hoạch quá chi tiết cho những gì chưa cần.

## Phase 3: Implement (surgical, minimal)
- Viết code tối thiểu cần thiết để đáp ứng success criteria
- Không thêm features "phòng hờ tương lai"
- Không refactor code không liên quan
- Match style của codebase hiện tại
- Sau mỗi bước lớn: verify checkpoint

## Phase 4: Test
- Tự kiểm tra happy path
- Tự kiểm tra edge cases đã identify ở Phase 1
- Nếu có test suite: chạy và đảm bảo pass
- Nếu không có test: viết ít nhất 1 test cho behavior quan trọng nhất

## Phase 5: Ship Checklist
- [ ] Code hoạt động đúng với success criteria đã định
- [ ] Không có debug logs, TODO, hoặc dead code
- [ ] Không có regression ở features liên quan
- [ ] Diff gọn gàng — chỉ những gì cần thiết

---
Output cuối: mô tả ngắn những gì đã làm và cách verify.

# /debug — Systematic Debugging

Bug cần debug: $ARGUMENTS

---

## Nguyên tắc: Không đoán. Chứng minh bằng evidence.

## Step 1: Reproduce (xác nhận bug tồn tại)
- Tìm cách reproduce bug một cách deterministic
- Nếu không reproduce được → không thể fix được
- Minimal reproduction case là gì?

## Step 2: Observe (thu thập data)
- Actual behavior: [gì đang xảy ra]
- Expected behavior: [gì nên xảy ra]
- Khi nào xảy ra / không xảy ra?
- Log, error message, stack trace đầy đủ

## Step 3: Hypothesize (đặt giả thuyết)
Liệt kê 3-5 nguyên nhân có thể, từ cao xuống thấp theo xác suất:
1. [Hypothesis A] — evidence ủng hộ: ..., evidence phản: ...
2. [Hypothesis B] — ...
3. ...

## Step 4: Test Hypotheses (systematic elimination)
Với mỗi hypothesis: thiết kế test nhỏ nhất có thể confirm/refute nó.
Không fix gì cho đến khi xác định được root cause.

## Step 5: Fix (surgical)
- Fix đúng root cause, không fix symptom
- Thay đổi tối thiểu
- Giải thích tại sao fix này đúng

## Step 6: Verify + Prevent
- Chạy lại reproduction case → bug không còn
- Kiểm tra regression
- Thêm test để bug này không tái xuất

---
Red flags cần tránh: "thử xem", "có thể là", fix-and-pray, thay đổi nhiều thứ cùng lúc.

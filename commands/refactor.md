# /refactor — Safe Surgical Refactor

Refactor target: $ARGUMENTS

---

## Nguyên tắc: Refactor = thay đổi structure, KHÔNG thay đổi behavior.

## Step 1: Define Scope (không mở rộng tùy tiện)
- Chính xác cái gì cần refactor và TẠI SAO
- Ranh giới rõ ràng: cái gì sẽ thay đổi, cái gì sẽ KHÔNG thay đổi
- Nếu không có lý do cụ thể → không refactor

## Step 2: Safety Net
- Tests hiện tại có cover behavior này không?
- Nếu không → viết characterization tests TRƯỚC KHI refactor
- "Không thay đổi behavior" phải verify được, không chỉ là lời nói

## Step 3: Refactor (từng bước nhỏ)
Mỗi bước:
1. Thay đổi nhỏ
2. Tests vẫn pass
3. Commit (hoặc checkpoint)
4. Bước tiếp theo

Không "big bang" refactor toàn bộ rồi mới test.

## Step 4: Code Quality Check
Sau refactor, kiểm tra:
- [ ] Behavior giống hệt trước (tests pass)
- [ ] Code dễ đọc hơn (hoặc ít nhất không tệ hơn)
- [ ] Không có abstractions mới chưa cần thiết
- [ ] Không có dead code mới

## Step 5: Diff Review
- Diff có gọn không? Có thay đổi ngoài scope không?
- Nếu có → revert những thay đổi ngoài scope

---
Nếu refactor dẫn đến "cần thay đổi thêm X, Y, Z" → dừng lại và tách thành các task riêng.

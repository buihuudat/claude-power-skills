# /think — Deep Reasoning Before Action

Before touching any code, reason through this task completely:

**Task:** $ARGUMENTS

---

## Step 1: Understand (không giả định gì cả)
- Bài toán thực sự đang yêu cầu là gì? (không phải những gì tôi nghĩ)
- Có bao nhiêu cách hiểu khác nhau về yêu cầu này?
- Đọc code liên quan, trace data flow, hiểu context đầy đủ trước khi viết bất kỳ dòng nào

## Step 2: Surface Hidden Complexity
- Những gì có vẻ đơn giản nhưng thực ra phức tạp?
- Edge cases nào chắc chắn sẽ xuất hiện?
- Dependencies nào sẽ bị ảnh hưởng?
- Có race conditions, state mutations, hoặc side effects không?

## Step 3: Multiple Approaches
Liệt kê ít nhất 3 cách tiếp cận khác nhau:
- Approach A: [đơn giản nhất]
- Approach B: [cân bằng]
- Approach C: [mạnh nhất nhưng phức tạp hơn]

Với mỗi approach: tradeoffs là gì? Khi nào nên dùng?

## Step 4: Recommendation
- Tôi đề xuất approach nào và TẠI SAO cụ thể với bài toán này
- Những điều tôi cần xác nhận trước khi bắt đầu

## Step 5: Success Criteria
Thay vì "fix the bug", định nghĩa thành công là:
- [ ] Test case X pass
- [ ] Behavior Y hoạt động đúng với input Z
- [ ] Không có regression ở module A, B

---
Chỉ bắt đầu implement SAU KHI đã hoàn thành tất cả 5 bước trên.

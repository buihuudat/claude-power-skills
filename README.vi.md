# ⚡ Claude Power Skills

> **9 slash commands thực chiến biến Claude Code thành senior engineer trong team của bạn.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Compatible-blue)](https://claude.ai/code)

---

## Tại Sao Cần Skills Này?

Claude (và hầu hết LLMs) có 3 thói quen xấu:

1. **Giả định thay vì hỏi** — lấp đầy ambiguity bằng đoán mò, build sai thứ
2. **Over-engineer** — thêm abstractions, patterns, "future-proofing" không ai yêu cầu
3. **Fix triệu chứng** — vá bug nhìn thấy mà không tìm root cause

Các skills này fix cả 3 bằng cách đưa cho Claude framework tư duy rõ ràng *trước* khi viết bất kỳ dòng code nào.

---

## Danh Sách Commands

| Command | Dùng khi nào | Làm gì |
|---|---|---|
| `/think` | Trước task phức tạp bất kỳ | Phân tích 5 bước: hiểu → surface complexity → 3 approaches → đề xuất → success criteria |
| `/ship` | Feature mới end-to-end | Clarify → plan → implement surgical → test → ship checklist |
| `/debug` | Bug chưa rõ root cause | Reproduce → observe → hypothesize → eliminate → fix → prevent |
| `/audit` | Review code / kiểm tra security | Correctness + security (OWASP) + performance + reliability |
| `/refactor` | Cải thiện cấu trúc code an toàn | Safety net trước → từng bước nhỏ → verify behavior không đổi |
| `/explain` | Hiểu code lạ | Big picture → data flow → design decisions → gotchas → cách modify an toàn |
| `/test` | Viết tests catch real bugs | Happy path → edge cases → error cases → regression → quality check |
| `/perf` | Tìm và fix bottleneck | Profile trước → complexity analysis → bottleneck checklist → measure |
| `/pr` | Tạo Pull Request | Diff review → title → description → test plan → self-review |

---

## Cài Đặt

### Cách 1: Global (khuyến nghị)

```bash
git clone https://github.com/YOUR_USERNAME/claude-power-skills.git
cp commands/*.md ~/.claude/commands/
```

Restart Claude Code. Dùng ngay.

### Cách 2: Chỉ cho project hiện tại

```bash
mkdir -p .claude/commands
cp /path/to/claude-power-skills/commands/*.md .claude/commands/
```

---

## Ví Dụ Thực Tế

### Không dùng skill (Claude đoán mò):
```
User: refactor payment service
Claude: [ngay lập tức bắt đầu refactor với assumptions chưa được confirm]
```

### Dùng `/think` (Claude tư duy trước):
```
/think refactor payment service to support multiple currencies
Claude: 
  Assumptions cần confirm: exchange rates stored where? Existing transactions affected?
  Approach A: wrapper layer (ít rủi ro, deploy dần)
  Approach B: schema migration (clean, nhưng cần downtime)  
  Approach C: ...
  Success criteria: test X pass, behavior Y verify được như thế nào...
```

---

## Triết Lý

> *"LLMs rất giỏi loop cho đến khi đạt được mục tiêu cụ thể. Đừng nói nó phải làm gì — hãy đưa ra success criteria và để nó tự xử lý."* — Andrej Karpathy

---

## License

MIT

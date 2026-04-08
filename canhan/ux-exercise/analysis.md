# UX exercise — MoMo Moni AI

## Sản phẩm: MoMo — Moni AI Assistant (phân loại chi tiêu)

## 4 paths

### 1. AI đúng
- User chi tiêu trong tháng 4 → Moni trả lời đúng
- User chưa phân loại -> Moni cho vào danh mục "Chưa phân loại"
- User phân loại giao dịch vào "Ăn uống" -> Moni cho vào danh mục "Ăn uống"

### 2. AI không chắc
- User nhập prompt "a" -> Moni trả lời "Bạn vừa gửi một chữ 'a' - chắc là đang thử Moni đúng không. Nếu bạn muốn kiểm tra chi tiêu, lập ngân sách, hay ..... Bạn muốn Moni giúp gì"


### 3. AI sai
- User đã lâu chưa có giao dịch, hỏi "giao dịch lần cuối của tôi trên Mono" -> Moni "Không có giao dịch nào được tìm thấy từ 2026-04-01 đến 2026-04-08"
- Sửa: User hỏi "mình muốn bạn tra cứu chi tiêu của mình trong quá khứ" → 4 bước → đổi category → 2 bước
- Vấn đề: không rõ AI hiểu intent của user

### 4. User mất niềm tin
- Khi user nói "chán" vì không trả lời ngày được giao dịch gần nhất -> Moni: Xin lỗi, và khẳng định luôn ở đây để trợ giúp user.

## Path yếu nhất: Path 3
- Khi AI sai do không hiểu intent của user.

## Gap marketing vs thực tế
- Marketing: "Moni giúp quản lý chi tiêu thông minh" nhưng khi hỏi giao dịch lần cuối giao dịch không trả lời đúng
- Gap lớn nhất: marketing không nói về khi AI sai — user kỳ vọng 100% chính xác

## Sketch
As-is
- User khó tìm được plugin Moni trên ứng dụng Mono
- AI auto-tag giao dịch
- User chỉ thấy kết quả cuối
- Sai thì user tự sửa
- Khi câu hỏi mơ hồ, AI trả lời không biết và hỏi lại
- Dễ hiểu sai intent
- Sai xong chỉ xin lỗi, khó lấy lại niềm tin
To-be
- AI auto-tag nhưng có kiểm tra confidence
- Confidence thấp thì hỏi user xác nhận
- Query mơ hồ thì clarify intent trước khi trả lời
- User correction được ghi nhận như tín hiệu học
- Khi AI sai, có flow recovery rõ ràng
- Trải nghiệm trung thực hơn với kỳ vọng “thông minh và đáng tin”


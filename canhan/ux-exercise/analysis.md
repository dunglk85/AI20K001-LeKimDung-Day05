# UX exercise — MoMo Moni AI

## Sản phẩm: MoMo — Moni AI Assistant (phân loại chi tiêu)

## 4 paths

### 1. AI đúng
- User chi tiêu 50k tại Circle K → Moni gợi ý "Ăn uống"
- User thấy tag đúng, không cần làm gì thêm
- UI: hiện tag + icon category, không hỏi confirm

### 2. AI không chắc
- User chuyển tiền 200k cho bạn → Moni không tag hoặc tag "Khác"
- UI: không hiện gợi ý nào, user phải tự vào chỉnh
- Vấn đề: không có cơ chế "bạn muốn phân loại giao dịch này không?"

### 3. AI sai
- User mua sách trên Shopee → Moni tag "Mua sắm" thay vì "Học tập"
- User phát hiện khi xem báo cáo tháng
- Sửa: vào chi tiết giao dịch → đổi category → 3 bước
- Vấn đề: không rõ AI có học từ correction này không

### 4. User mất niềm tin
- Sau nhiều lần tag sai, user không tin báo cáo chi tiêu tự động nữa
- Không có option "tắt auto-tag" hoặc "tag thủ công trước"
- Không có fallback rõ ràng ngoài việc sửa từng giao dịch

## Path yếu nhất: Path 3 + 4
- Khi AI sai, recovery flow mất quá nhiều bước
- Không có feedback loop rõ — user sửa nhưng không biết AI có học không
- Không có exit/fallback cho user mất niềm tin

## Gap marketing vs thực tế
- Marketing: "Moni giúp quản lý chi tiêu thông minh"
- Thực tế: auto-tag chỉ đúng ~70% cho giao dịch phổ biến, các trường hợp edge case
  (chuyển tiền, mua online) thường bị tag sai hoặc không tag
- Gap lớn nhất: marketing không nói về khi AI sai — user kỳ vọng 100% chính xác

## Sketch
(Ảnh đính kèm: sketch.jpg)
- As-is: giao dịch → auto-tag → user thấy kết quả → nếu sai phải vào sửa thủ công
- To-be: giao dịch → auto-tag → nếu confidence thấp: hiện "Bạn muốn phân loại?"
  → user chọn → AI ghi nhận correction → hiện "Đã học, lần sau sẽ chính xác hơn"
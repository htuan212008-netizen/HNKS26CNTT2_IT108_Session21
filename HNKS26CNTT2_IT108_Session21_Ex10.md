# Bài 10: Đánh Giá Đa Giải Pháp Quy Trình Khắc Phục Sự Cố Kỹ Thuật
## Phần 1: Lập bảng So sánh Trade-off Toàn diện
1. Bảng so sánh chi tiết

| Tiêu chí đánh giá | Phương án 1: Hỗ trợ Cảm tính / Nhóm Chat | Phương án 2: Troubleshooting 4 Chặng Chuẩn hóa |
| :--- | :--- | :--- |
| **1. Thời gian xử lý sự cố (Downtime)** | Kéo dài — Phụ thuộc vào việc Senior Dev có rảnh để trả lời hay không | Rút ngắn 80% — Tự giải quyết tại chỗ trong 5-10 phút đầu tiên |
| **2. Áp lực & Chi phí cho Senior Devs** | Rất cao — Bị phân tâm liên tục bởi các câu hỏi lỗi cơ bản lặp lại | Tối ưu — Senior chỉ tiếp nhận các ca lỗi phức tạp có Bug Report chuẩn |
| **3. Năng lực & Tính tự chủ của KTV** | Thụ động, sợ hãi thông báo lỗi tiếng Anh, không tiến bộ nghề nghiệp | Chủ động, tư duy phân tích sắc bén, làm chủ trọn vẹn máy tính trạm |
| **4. Khả năng lưu vết tri thức (Knowledge Base)** | Thất thoát — Tin nhắn trôi mất trên Zalo, người sau gặp lại lỗi cũ | Lưu trữ tập trung — Tích lũy tài liệu Wiki sửa lỗi nội bộ công ty |
2. Kết luận
- Tối ưu chi phí
- Giải phóng nguồn lực
- Xây dựng hệ thống tự chủ
## Phần 2: Thiết kế Sơ đồ Luồng Ra Quyết Định
3. Sơ đồ
KIOSK GẶP SỰ CỐ
- Chặng 1: Bóc tách từ khóa & Googling
      => Sử dụng toán tử nâng cao (site:, "", dấu trừ -) để tìm kiếm chính xác trên web.

- Chặng 2: Thẩm định StackOverflow / GitHub Issues
       => Áp dụng quy tắc đọc lướt 30s, ưu tiên bài viết có tích xanh (✓) hoặc nhiều Upvote.
       => [Thành công] ──► Xử lý dứt điểm tại chỗ.
       => [Chưa rõ]    ──► Chuyển sang Chặng 3.
  
- Chặng 3: Giải mã thông báo lỗi cùng Trợ lý AI
       => Gửi Prompt 3 thành phần chuẩn hóa (Context + Raw Error + Instruction) lấy tiếng Việt.
       => [Thành công] ──► Khôi phục hoạt động trạm sạc.
       => [Thất bại sau 15 phút] ──► Chuyển sang Chặng 4.

- Chặng 4: Lập phiếu Bug Report chuẩn hóa gửi IT Helpdesk
       => Điền đầy đủ framework 4 bước (Bối cảnh => Mong muốn => Thực tế => Log lỗi) gửi về cấp cao.

# Bài 4: Đánh giá công cụ hỗ trợ xử lý lỗi lập trình

## 1. Bảng so sánh Ưu/Nhược điểm

| Tiêu chí | Google Search (StackOverflow/Docs) | AI Assistant (ChatGPT/Gemini) |
| :--- | :--- | :--- |
| **Độ chính xác** | **Cao:** Tài liệu gốc hoặc bài đăng đã được cộng đồng kiểm chứng thực tế. | **Khá cao:** Thường chính xác với lỗi phổ biến, nhưng đôi khi bịa đặt thông tin. |
| **Tính cập nhật** | **Rất cao:** Tìm kiếm được các bài thảo luận, bản vá hoặc lỗi mới phát sinh ngay lập tức. | **Phụ thuộc dữ liệu huấn luyện:** Có thể thiếu thông tin về các công nghệ hoặc phiên bản mới ra mắt. |
| **Khả năng giải thích** | **Thấp - Trung bình:** Đòi hỏi người dùng tự đọc, tổng hợp và hiểu nhiều bài viết khác nhau. | **Rất cao:** Giải thích chi tiết nguyên nhân gốc rễ, ngữ cảnh và từng bước khắc phục trực quan. |
| **Rủi ro (Hallucination)** | **Thấp:** Hiếm khi sai lệch thông tin cốt lõi nếu chọn đúng nguồn uy tín. | **Có rủi ro:** Có thể sinh ra mã lệnh sai hoặc hướng dẫn lệnh không tồn tại trên hệ thống. |

---

## 2. Lựa chọn trường hợp bắt buộc dùng Google Search để đảm bảo an toàn máy tính

- **Trường hợp bắt buộc:** Khi cần chạy các **lệnh can thiệp sâu vào hệ thống** (như sửa Registry Windows, phân vùng ổ cứng,
cấp quyền Root/Sudo xóa file hệ thống, hoặc gỡ cài đặt các dịch vụ cốt lõi) do AI đề xuất nhưng chưa được kiểm chứng.
- **Lý do:** Tránh việc AI bịa ra tham số lệnh nguy hiểm (Hallucination) dẫn đến mất dữ liệu, lỗi hệ điều hành hoặc hỏng môi
- trường phát triển cục bộ. Google Search giúp đối chiếu trực tiếp từ tài liệu chính thống của nhà phát triển hoặc các kỹ sư có kinh nghiệm trên diễn đàn uy tín.

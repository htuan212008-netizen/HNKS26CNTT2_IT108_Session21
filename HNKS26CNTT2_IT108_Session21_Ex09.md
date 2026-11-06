# Bài 9: Xây Dựng Prompt 3 Thành Phần Giải Mã Thông Báo Lỗi Trạm Sạc Cùng Trợ Lý AI

## Phần 1: Thiết kế Prompt 3 Thành Phần Chuẩn Hóa

1. Nguyên nhân vì sao câu hỏi cụt ngủn gây ra lỗi ảo giác (Hallucination)
* Thiếu thông tin ngữ cảnh (`Context`) về hệ điều hành, môi trường phần mềm và đoạn log lỗi thực tế.
* Khiến AI phải phỏng đoán mù quáng, đưa ra giải pháp chung chung, nguy hiểm hoặc sai lệch hoàn toàn bản chất vấn đề (ví dụ: khuyên tháo phần cứng trạm sạc thay vì xử lý phân quyền file phần mềm).

2. Mẫu Prompt 3 Thành Phần Hoàn Chỉnh
```text
Tôi đang vận hành ứng dụng phần mềm điều khiển trạm sạc điện trên hệ điều hành Windows 11 thì gặp lỗi ".....".

Hãy dịch nghĩa thông báo lỗi này sang tiếng Việt đơn giản, giải thích nguyên nhân gốc rễ và hướng dẫn 3 bước khắc phục cụ thể.
```
## Phần 2: Giải mã Lỗi & Kịch bản Khắc phục
3. Lỗi ngoại lệ không được cấp quyền truy cập. Ứng dụng ghi vào file mà không chạy dưới quyền admin dẫn đến hệ điều hành chặn thao tác ghi file.
4. Cách khắc phục trên Win 11:
- Cách 1: Ấn chuột phải vào app và chọn Run as administrator
- Cách 2: Mở thư mục, nhấp chuột phải chọn Propoties, tab Security chọn Edit và cấp Full control cho tài khoản hiện tại.
- Cách 3: Chuyển file log ra vị trí khạc

# Bài 3: Ứng dụng mô hình IPO trong xử lý lỗi Git
## Báo cáo phân tích IPO
- Input:
1. Ngữ cảnh: Thao tác dòng lệnh với Git trong dự án cá nhân
2. Mã lỗi: `fatal: not a git repository (or any of the parent directories): .git`
- Process: AI phân tích lỗi, dịch nghĩa và giải thích nguyên nhân gốc rễ. Sau đó đưa ra hướng khắc phục.
- Output:
1. Bản dịch: Không phải là kho chứa git
2. 3 bước khắc phục: Đầu tiên kiểm tra lại đường dẫn thư mục hiện tại, di chuyển vào đúng thư mục và khởi tạo Git
  ## Câu prompt chuẩn
  > Tôi là newbie, viết code gặp lỗi **"fatal: not a git repository (or any of the parent directories): .git"**. Hãy đưa ra nguyên nhân và hướng khắc phục cho tôi

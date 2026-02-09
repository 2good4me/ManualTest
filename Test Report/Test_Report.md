# Báo cáo kiểm thử (Test Report)
**Dự án**: Swag Labs (https://www.saucedemo.com)
**Ngày báo cáo**: 04/02/2026

## 1. Tổng quan
Đợt kiểm thử thực hiện trên trang Swag Labs, tập trung vào việc kiểm thử các kịch bản người dùng khác nhau (`standard`, `problem`, `locked_out`) được cung cấp bởi nền tảng.

## 2. Kết quả thực thi
| Loại | Số lượng | Tỷ lệ (%) |
| :--- | :--- | :--- |
| **Tổng số TC** | 35 | 100% |
| **Đạt (Pass)** | 28 | 80% |
| **Trượt (Fail)** | 7 | 20% |
*(Fail do test trên các user bị lỗi cố ý như problem_user)*

## 3. Top 5 lỗi điển hình
1.  **BUG_AUTH_001**: Tài khoản `locked_out_user` bị chặn đăng nhập (Đây là tính năng, nhưng log thành bug để tracking behavior).
2.  **BUG_UI_002**: Ảnh sản phẩm bị lỗi (hình con chó) khi dùng `problem_user`.
3.  **BUG_CHK_003**: Không thể nhập đúng Last Name (bị ghi đè ký tự) khi dùng `problem_user`.
4.  **BUG_PROD_004**: Hiệu năng tải trang chậm khi dùng `performance_glitch_user`.
5.  **BUG_PROD_009**: Chức năng Sort Z-A không hoạt động với `problem_user`.

## 4. Nhận xét chất lượng
*   **Standard User**: Hoạt động hoàn hảo, không có lỗi.
*   **Special Users**: Hệ thống mô phỏng chính xác các lỗi (Error, Glitch, Lock) theo thiết kế test của Sauce Labs.

## 5. Kết luận
✅ **RELEASE** (Có thể phát hành - Với Standard User)

**Ghi chú**: Các lỗi tìm thấy ở trên là các lỗi "dự kiến" (Expected Bugs) của trang web demo này nhằm mục đích đào tạo. Nếu đây là sản phẩm thật, các bug này đều là Critical/Major.

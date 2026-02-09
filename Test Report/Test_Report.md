

## 1. Tổng quan
Đợt kiểm thử tập trung vào các luồng nghiệp vụ chính trên trang Automation Exercise: User Flow (Đăng ký/Login), Product Flow (Tìm kiếm/Lọc) và Checkout Flow (Thanh toán giả lập).

## 2. Kết quả thực thi
| Loại | Số lượng | Tỷ lệ (%) |
| :--- | :--- | :--- |
| **Tổng số TC** | 45 | 100% |
| **Đạt (Pass)** | 35 | 77.8% |
| **Trượt (Fail)** | 10 | 22.2% |
| **Chặn (Blocked)** | 0 | 0% |

## 3. Top 5 lỗi nghiêm trọng nhất
*(Dựa trên danh sách lỗi đã tìm thấy trong quá trình test thực tế/giả lập)*

1.  **BUG_CHK_004** (Nghiêm trọng): Lỗi Double Submission khi nhấn nút Pay nhiều lần, tạo đơn trùng.
2.  **BUG_CART_008** (Nghiêm trọng): Hệ thống tính sai tiền khi nhập số lượng là số thập phân (2.5).
3.  **BUG_PROD_002** (Lớn): Tìm kiếm sản phẩm không nhất quán giữa chữ Hoa và chữ Thường.
4.  **BUG_AUTH_005** (Lớn): Form đăng ký nhận tin (Subscription) chấp nhận email sai định dạng.
5.  **BUG_UI_006** (Lớn): Banner quảng cáo che khuất menu điều hướng trên giao diện Mobile.

## 4. Nhận xét chất lượng
*   **Chức năng**: Các luồng happy path hoạt động trơn tru. Tuy nhiên logic xử lý các trường hợp biên (số thập phân, submit liên tục) chưa tốt.
*   **Giao diện**: Gặp vấn đề hiển thị trên Mobile do quảng cáo chèn vào nội dung. Font chữ chưa đồng bộ ở một số trang con.
*   **Bảo mật**: Các form input cần validation chặt chẽ hơn (Subscription, Login password clear).

## 5. Kết luận & Quyết định
❌ **KHÔNG PHÁT HÀNH (NO-RELEASE)**

**Lý do**: Tồn tại lỗi nghiêm trọng liên quan đến Thanh toán (Double Submission) và Tính toán giá tiền (Decimal quantity). Cần đội Dev khắc phục các lỗi Critical này trước khi Release.

# KẾ HOẠCH KIỂM THỬ (TEST PLAN)
**Dự án**: Website Swag Labs (https://www.saucedemo.com)
**Phiên bản**: 2.0
**Ngày tạo**: 04/02/2026

---

## 1. GIỚI THIỆU
Tài liệu này mô tả kế hoạch kiểm thử cho dự án Website **Swag Labs** (còn gọi là SauceDemo). Đây là trang web mẫu của Sauce Labs mô phỏng cửa hàng bán đồ lưu niệm, được thiết kế đặc biệt để thực hành kiểm thử với các kịch bản lỗi có sẵn.

Đối tượng của tài liệu này bao gồm: Đội quản lý dự án, Đội phát triển, và Đội kiểm thử.

## 2. PHẠM VI KIỂM THỬ

### 2.1 Trong phạm vi
Các chức năng chính sẽ được kiểm thử trên trang https://www.saucedemo.com bao gồm:
*   **Module 1: Xác thực (Authentication)**
    *   Đăng nhập với nhiều loại tài khoản:
        *   `standard_user` (Người dùng chuẩn).
        *   `locked_out_user` (Người dùng bị khóa).
        *   `problem_user` (Người dùng gặp lỗi hệ thống).
        *   `performance_glitch_user` (Người dùng gặp lỗi hiệu năng).
    *   Đăng xuất (Logout).
*   **Module 2: Sản phẩm & Giỏ hàng (Products & Cart)**
    *   Trang "Inventory": Sắp xếp (Sort) sản phẩm (A-Z, Z-A, Price).
    *   Trang "Item Detail": Xem chi tiết, Back to products.
    *   Trang "Cart": Thêm, Xóa sản phẩm.
*   **Module 3: Thanh toán (Checkout)**
    *   Bước 1: Your Information (Nhập tên, Zip code).
    *   Bước 2: Overview (Xem lại đơn hàng, phí thuế).
    *   Bước 3: Finish (Hoàn tất).

### 2.2 Ngoài phạm vi / Không áp dụng
*   **Chức năng Đăng ký (Sign Up)**: Trang web này không hỗ trợ đăng ký mới (Sử dụng tài khoản có sẵn).
*   Chức năng Quên mật khẩu (Không hỗ trợ).
*   Kiểm thử hiệu năng, bảo mật chuyên sâu.

## 3. PHƯƠNG PHÁP KIỂM THỬ

### 3.1 Kiểm thử chức năng
*   Kiểm tra luồng đi (Happy Path) của chức năng mua hàng với `standard_user`.
*   Kiểm tra các luồng lỗi (Exception Path) với các user đặc biệt (`locked_out`, `problem`).

### 3.2 Kiểm thử giao diện
*   Kiểm tra việc hiển thị hình ảnh sản phẩm (đặc biệt với `problem_user` sẽ bị lỗi ảnh).
*   Kiểm tra Responsive trên Chrome/Mobile view.

## 4. MÔI TRƯỜNG KIỂM THỬ

| Thành phần | Chi tiết |
| :--- | :--- |
| **URL Kiểm thử** | **https://www.saucedemo.com** |
| **Phần cứng** | Máy tính Windows Tiêu chuẩn |
| **Trình duyệt** | Google Chrome, Firefox, Edge |
| **Dữ liệu kiểm thử** | Account: `standard_user`, `locked_out_user`, `problem_user`, `error_user`, `visual_user` / Pass: `secret_sauce` |
| **Công cụ** | Excel, Snipping Tool |

## 5. ĐIỀU KIỆN VÀO / RA

### 5.1 Điều kiện bắt đầu
*   Website truy cập bình thường.
*   Nắm rõ các username và behavior (hành vi) của từng user.

### 5.2 Điều kiện kết thúc
*   Hoàn thành 100% Test Case đã thiết kế.
*   Báo cáo các bug đặc trưng của trang (như lỗi ảnh chó, lỗi sort,...).

## 6. RỦI RO & BIỆN PHÁP GIẢM THIỂU

| Rủi ro | Mức độ | Biện pháp giảm thiểu |
| :--- | :--- | :--- |
| Không có chức năng đăng ký, thiếu case về Register | Cao | Bổ sung case về Login với nhiều kịch bản (User bị khóa, sai pass) để bù đắp số lượng. |
| User session có thể bị reset khi refresh | Thấp | Test liên tục, không refresh nếu không cần thiết. |

## 7. VAI TRÒ & TRÁCH NHIỆM
*   QA Team: Thực hiện test thủ công.

## 8. LỊCH TRÌNH KIỂM THỬ
*   04/02/2026: Cập nhật tài liệu.
*   05/02/2026: Thực thi test trên Swag Labs.
*   06/02/2026: Báo cáo.

---
**Phê duyệt bởi**: _________________ (Job Lead)

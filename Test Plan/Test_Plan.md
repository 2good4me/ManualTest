# KẾ HOẠCH KIỂM THỬ (TEST PLAN)
**Dự án**: Website Automation Exercise (https://automationexercise.com)
**Phiên bản**: 1.1
**Ngày tạo**: 04/02/2026

---

## 1. GIỚI THIỆU
Tài liệu này mô tả kế hoạch kiểm thử cho dự án Website **Automation Exercise**. Đây là một trang web thương mại điện tử thực tế được sử dụng để thực hành kiểm thử tự động và thủ công. Mục đích là xác định phạm vi, phương pháp, tài nguyên và lịch trình cho quá trình kiểm thử thủ công.

Đối tượng của tài liệu này bao gồm: Đội quản lý dự án, Đội phát triển, và Đội kiểm thử.

## 2. PHẠM VI KIỂM THỬ

### 2.1 Trong phạm vi
Các chức năng chính sẽ được kiểm thử trên trang https://automationexercise.com bao gồm:
*   **Module 1: Xác thực (Authentication)**
    *   Trang "Signup / Login".
    *   Đăng ký tài khoản mới (New User Signup).
    *   Đăng nhập tài khoản (Login to your account).
    *   Đăng xuất (Logout).
*   **Module 2: Sản phẩm & Giỏ hàng (Products & Cart)**
    *   Trang "Products": Tìm kiếm, lọc danh mục (Category/Brand).
    *   Trang "Product Details": Xem chi tiết.
    *   Trang "Cart": Thêm, cập nhật số lượng, xóa sản phẩm.
*   **Module 3: Thanh toán (Checkout)**
    *   Quy trình "Proceed to Checkout".
    *   Nhập địa chỉ giao hàng.
    *   Thanh toán (Payment).
    *   Xóa tài khoản (phụ/nếu có).

### 2.2 Ngoài phạm vi
*   Kiểm thử hiệu năng (Tải/Chịu tải).
*   Kiểm thử bảo mật chuyên sâu.
*   Kiểm thử tự động (Automation) - *Trừ khi có yêu cầu riêng*.
*   Các liên kết quảng cáo (Ads) trên trang.

## 3. PHƯƠNG PHÁP KIỂM THỬ

### 3.1 Kiểm thử chức năng
*   Đảm bảo tất cả các luồng hoạt động đúng trên môi trường Live.
*   Thực hiện kiểm thử các trường hợp hợp lệ và không hợp lệ.

### 3.2 Kiểm thử giao diện
*   Kiểm tra tính hiển thị trên trình duyệt Chrome.
*   Kiểm tra độ phản hồi (Responsive) cơ bản.

### 3.3 Kiểm thử hồi quy
*   Thực hiện Kiểm tra khói (Smoke Test) trên các luồng chính.

## 4. MÔI TRƯỜNG KIỂM THỬ

| Thành phần | Chi tiết |
| :--- | :--- |
| **URL Kiểm thử** | **https://automationexercise.com** |
| **Phần cứng** | Máy tính Windows Tiêu chuẩn |
| **Hệ điều hành** | Windows 10/11 |
| **Trình duyệt** | Google Chrome (Phiên bản mới nhất) |
| **Mạng** | Internet ổn định (Truy cập Web Online) |
| **Dữ liệu kiểm thử** | Tự tạo tài khoản test (Register New User) |
| **Công cụ kiểm thử** | Excel/Google Sheets, Chụp màn hình (Snipping Tool) |

## 5. ĐIỀU KIỆN VÀO / RA

### 5.1 Điều kiện bắt đầu
*   Website https://automationexercise.com hoạt động bình thường.
*   Tài liệu yêu cầu (dựa trên chức năng của web) đã được hiểu rõ.
*   Môi trường mạng ổn định.

### 5.2 Điều kiện kết thúc
*   100% Ca kiểm thử Critical/High đã thực thi.
*   Báo cáo đầy đủ các lỗi tìm thấy trên trang web thực tế.

## 6. RỦI RO & BIỆN PHÁP GIẢM THIỂU

| Rủi ro | Mức độ | Biện pháp giảm thiểu |
| :--- | :--- | :--- |
| Website bảo trì hoặc không truy cập được | Trung bình | Kiểm tra trạng thái web trước khi test. Chụp ảnh màn hình làm bằng chứng. |
| Dữ liệu test bị xóa định kỳ (do là web demo) | Thấp | Tạo dữ liệu mới mỗi lần test (Luôn bắt đầu bằng Signup). |
| Quảng cáo che khuất phần tử | Cao | Sử dụng Adblock nếu được phép hoặc test cẩn thận trên Mobile. |

## 7. VAI TRÒ & TRÁCH NHIỆM

*   **Trưởng nhóm QA**: Lên kế hoạch, xem xét Ca kiểm thử.
*   **Nhân viên kiểm thử**: Thực thi test trên web Automation Exercise, log bug.
*   *(Lưu ý: Không có Developer fix bug vì đây là web public)*

## 8. LỊCH TRÌNH KIỂM THỬ

| Hoạt động | Ngày bắt đầu | Ngày kết thúc | Trách nhiệm |
| :--- | :--- | :--- | :--- |
| Tìm hiểu cấu trúc web Automation Exercise | 01/02/2026 | 02/02/2026 | Nhóm QA |
| Cập nhật Test Case cho phù hợp | 03/02/2026 | 05/02/2026 | Nhóm QA |
| Thực thi Test trên web thật | 06/02/2026 | 08/02/2026 | Nhóm QA |
| Tổng hợp Báo cáo & Metrics | 13/02/2026 | 13/02/2026 | Trưởng nhóm QA |

---
**Phê duyệt bởi**: _________________ (Quản lý dự án)

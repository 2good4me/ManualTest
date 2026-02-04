
## 1. GIỚI THIỆU (INTRODUCTION)
Tài liệu này mô tả kế hoạch kiểm thử cho dự án Website E-commerce. Mục đích là xác định phạm vi, phương pháp, tài nguyên và lịch trình cho quá trình kiểm thử thủ công (manual testing) để đảm bảo chất lượng phần mềm trước khi phát hành.

Đối tượng của tài liệu này bao gồm: Đội quản lý dự án (PM), Đội phát triển (Dev), và Đội kiểm thử (QA/QC).

## 2. PHẠM VI KIỂM THỬ (SCOPE)

### 2.1 Trong phạm vi (In-scope)
Các chức năng chính sẽ được kiểm thử bao gồm các module sau:
*   **Module 1: Xác thực (Authentication)**
    *   Đăng ký, Đăng nhập, Đăng xuất, Quên mật khẩu.
*   **Module 2: Sản phẩm & Giỏ hàng (Product & Cart)**
    *   Tìm kiếm, Lọc sản phẩm, Xem chi tiết.
    *   Thêm/Sửa/Xóa sản phẩm trong giỏ hàng.
*   **Module 3: Thanh toán (Checkout)**
    *   Đặt hàng, Thanh toán, Lịch sử đơn hàng.

### 2.2 Ngoài phạm vi (Out-of-scope)
*   Kiểm thử hiệu năng (Performance/Load Testing).
*   Kiểm thử bảo mật chuyên sâu (Penetration Testing).
*   Kiểm thử tự động (Automation Testing).
*   Các tích hợp API bên thứ 3 thực tế (Sử dụng giả lập cho thanh toán).

## 3. PHƯƠNG PHÁP KIỂM THỬ (TEST APPROACH)

### 3.1 Kiểm thử chức năng (Functional Testing)
*   Đảm bảo tất cả các yêu cầu (Requirements) hoạt động đúng như mô tả.
*   Thực hiện kiểm thử các trường hợp tích cực (Positive) và tiêu cực (Negative).
*   Kiểm thử giá trị biên (Boundary Value Analysis).

### 3.2 Kiểm thử giao diện (UI/UX Testing - Basic)
*   Kiểm tra tính nhất quán của giao diện, font chữ, màu sắc, bố cục trên trình duyệt Chrome.
*   Kiểm tra validation message.

### 3.3 Kiểm thử hồi quy (Regression Testing)
*   Thực hiện Smoke Test khi có build mới.
*   Thực hiện Regression Test các chức năng bị ảnh hưởng sau khi fix bug.

## 4. MÔI TRƯỜNG KIỂM THỬ (TEST ENVIRONMENT)

| Thành phần | Chi tiết |
| :--- | :--- |
| **Phần cứng** | PC/Laptop Windows Standard |
| **Hệ điều hành** | Windows 10/11 |
| **Trình duyệt** | Google Chrome (Latest Version) |
| **Mạng** | Wifi/LAN ổn định |
| **Dữ liệu test** | Tài khoản giả lập (User/Admin), Dữ liệu sản phẩm mẫu |
| **Test Tool** | Excel/Google Sheets (quản lý TC), Bug Tracking System (Giả lập) |

## 5. ĐIỀU KIỆN VÀO / RA (ENTRY / EXIT CRITERIA)

### 5.1 Điều kiện bắt đầu (Entry Criteria)
*   Đội phát triển đã deploy bản build lên môi trường Test (Staging).
*   Tài liệu yêu cầu (Requirement) đã được phê duyệt.
*   Môi trường Test đã sẵn sàng và truy cập được.

### 5.2 Điều kiện kết thúc (Exit Criteria)
*   100% Test Case mức độ Priority High/Critical đã được thực thi.
*   Tỷ lệ Pass các Test Case High/Critical đạt 100%.
*   Độ bao phủ yêu cầu (Requirement Coverage) > 90%.
*   Không còn lỗi nghiêm trọng (Severity: Critical/Major) chưa được fix (trừ khi có sự chấp thuận của PM).

## 6. RỦI RO & BIỆN PHÁP GIẢM THIỂU (RISKS & MITIGATION)

| Rủi ro | Mức độ | Biện pháp giảm thiểu |
| :--- | :--- | :--- |
| Thiếu hụt thời gian kiểm thử do Dev giao build trễ | Cao | Ưu tiên test các luồng chính (Happy Path) và chức năng quan trọng trước. OT nếu cần thiết. |
| Yêu cầu thay đổi thường xuyên | Trung bình | Yêu cầu đóng băng yêu cầu (Feature freeze) trước giai đoạn test cuối. Cập nhật RTM liên tục. |
| Môi trường test không ổn định | Trung bình | Yêu cầu đội Dev hỗ trợ trực (standby) trong giai đoạn test cao điểm. |

## 7. VAI TRÒ & TRÁCH NHIỆM (ROLES & RESPONSIBILITIES)

*   **QA Leader**: Lên kế hoạch (Test Plan), review Test Case, báo cáo kết quả (Test Report).
*   **QA Tester**: Thiết kế Test Case, thực thi Test (Execute), Log bug, Verify bug fix.
*   **Developer**: Fix bug, hỗ trợ môi trường.

## 8. LỊCH TRÌNH KIỂM THỬ GIẢ LẬP (TEST SCHEDULE)

| Hoạt động | Ngày bắt đầu | Ngày kết thúc | Trách nhiệm |
| :--- | :--- | :--- | :--- |
| Phân tích yêu cầu & Lập Test Plan | 01/02/2026 | 02/02/2026 | QA Lead |
| Thiết kế Test Case | 03/02/2026 | 05/02/2026 | QA Team |
| Thực thi Test (Round 1) | 06/02/2026 | 08/02/2026 | QA Team |
| Fix Bug & Deploy | 09/02/2026 | 10/02/2026 | Dev Team |
| Regression Test (Round 2) | 11/02/2026 | 12/02/2026 | QA Team |
| Tổng hợp Test Report | 13/02/2026 | 13/02/2026 | QA Lead |

---
**Phê duyệt bởi**: _________________ (Project Manager)

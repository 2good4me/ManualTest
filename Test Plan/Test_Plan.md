## 1. GIỚI THIỆU
Tài liệu này mô tả kế hoạch kiểm thử cho dự án Website E-commerce. Mục đích là xác định phạm vi, phương pháp, tài nguyên và lịch trình cho quá trình kiểm thử thủ công để đảm bảo chất lượng phần mềm trước khi phát hành.

Đối tượng của tài liệu này bao gồm: Đội quản lý dự án, Đội phát triển, và Đội kiểm thử.

## 2. PHẠM VI KIỂM THỬ

### 2.1 Trong phạm vi
Các chức năng chính sẽ được kiểm thử bao gồm các module sau:
*   **Module 1: Xác thực**
    *   Đăng ký, Đăng nhập, Đăng xuất, Quên mật khẩu.
*   **Module 2: Sản phẩm & Giỏ hàng**
    *   Tìm kiếm, Lọc sản phẩm, Xem chi tiết.
    *   Thêm/Sửa/Xóa sản phẩm trong giỏ hàng.
*   **Module 3: Thanh toán**
    *   Đặt hàng, Thanh toán, Lịch sử đơn hàng.

### 2.2 Ngoài phạm vi
*   Kiểm thử hiệu năng (Tải/Chịu tải).
*   Kiểm thử bảo mật chuyên sâu.
*   Kiểm thử tự động.
*   Các tích hợp API bên thứ 3 thực tế (Sử dụng giả lập cho thanh toán).

## 3. PHƯƠNG PHÁP KIỂM THỬ

### 3.1 Kiểm thử chức năng
*   Đảm bảo tất cả các yêu cầu hoạt động đúng như mô tả.
*   Thực hiện kiểm thử các trường hợp hợp lệ và không hợp lệ.
*   Kiểm thử giá trị biên.

### 3.2 Kiểm thử giao diện
*   Kiểm tra tính nhất quán của giao diện, font chữ, màu sắc, bố cục trên trình duyệt Chrome.
*   Kiểm tra thông báo xác thực.

### 3.3 Kiểm thử hồi quy
*   Thực hiện Kiểm tra khói (Smoke Test) khi có bản dựng mới.
*   Thực hiện Kiểm thử hồi quy các chức năng bị ảnh hưởng sau khi sửa lỗi.

## 4. MÔI TRƯỜNG KIỂM THỬ

| Thành phần | Chi tiết |
| :--- | :--- |
| **Phần cứng** | Máy tính Windows Tiêu chuẩn |
| **Hệ điều hành** | Windows 10/11 |
| **Trình duyệt** | Google Chrome (Phiên bản mới nhất) |
| **Mạng** | Wifi/LAN ổn định |
| **Dữ liệu kiểm thử** | Tài khoản giả lập (Người dùng/Quản trị), Dữ liệu sản phẩm mẫu |
| **Công cụ kiểm thử** | Excel/Google Sheets (quản lý ca kiểm thử), Hệ thống theo dõi lỗi (Giả lập) |

## 5. ĐIỀU KIỆN VÀO / RA

### 5.1 Điều kiện bắt đầu
*   Đội phát triển đã triển khai bản dựng lên môi trường Kiểm thử (Staging).
*   Tài liệu yêu cầu đã được phê duyệt.
*   Môi trường Kiểm thử đã sẵn sàng và truy cập được.

### 5.2 Điều kiện kết thúc
*   100% Ca kiểm thử mức độ Ưu tiên Cao/Nghiêm trọng đã được thực thi.
*   Tỷ lệ Đạt các Ca kiểm thử Cao/Nghiêm trọng đạt 100%.
*   Độ bao phủ yêu cầu > 90%.
*   Không còn lỗi nghiêm trọng (Nghiêm trọng/Lớn) chưa được sửa (trừ khi có sự chấp thuận của Quản lý dự án).

## 6. RỦI RO & BIỆN PHÁP GIẢM THIỂU

| Rủi ro | Mức độ | Biện pháp giảm thiểu |
| :--- | :--- | :--- |
| Thiếu hụt thời gian kiểm thử do Dev giao bản dựng trễ | Cao | Ưu tiên kiểm tra các luồng chính và chức năng quan trọng trước. Làm thêm giờ nếu cần thiết. |
| Yêu cầu thay đổi thường xuyên | Trung bình | Yêu cầu đóng băng chức năng trước giai đoạn kiểm tra cuối. Cập nhật RTM liên tục. |
| Môi trường kiểm thử không ổn định | Trung bình | Yêu cầu đội Dev hỗ trợ trực trong giai đoạn kiểm tra cao điểm. |

## 7. VAI TRÒ & TRÁCH NHIỆM

*   **Trưởng nhóm QA**: Lên kế hoạch, xem xét Ca kiểm thử, báo cáo kết quả.
*   **Nhân viên kiểm thử (QA Tester)**: Thiết kế Ca kiểm thử, thực thi Kiểm thử, Ghi nhận lỗi, Xác minh sửa lỗi.
*   **Lập trình viên (Developer)**: Sửa lỗi, hỗ trợ môi trường.

## 8. LỊCH TRÌNH KIỂM THỬ GIẢ LẬP

| Hoạt động | Ngày bắt đầu | Ngày kết thúc | Trách nhiệm |
| :--- | :--- | :--- | :--- |
| Phân tích yêu cầu & Lập Kế hoạch | 01/02/2026 | 02/02/2026 | Trưởng nhóm QA |
| Thiết kế Ca kiểm thử | 03/02/2026 | 05/02/2026 | Nhóm QA |
| Thực thi Kiểm thử (Vòng 1) | 06/02/2026 | 08/02/2026 | Nhóm QA |
| Sửa lỗi & Triển khai | 09/02/2026 | 10/02/2026 | Nhóm Dev |
| Kiểm thử hồi quy (Vòng 2) | 11/02/2026 | 12/02/2026 | Nhóm QA |
| Tổng hợp Báo cáo kiểm thử | 13/02/2026 | 13/02/2026 | Trưởng nhóm QA |

---
**Phê duyệt bởi**: _________________ (Quản lý dự án)

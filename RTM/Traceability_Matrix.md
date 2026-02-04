# Ma trận truy vết yêu cầu (RTM)

| Mã Yêu cầu | Yêu cầu | Mã TC (Ánh xạ) | Trạng thái Bao phủ |
| :--- | :--- | :--- | :--- |
| **R1** | Người dùng đăng ký bằng email hợp lệ | TC_AUTH_001, TC_AUTH_014, TC_AUTH_005 | Đã bao phủ |
| **R2** | Không cho đăng ký khi email sai định dạng | TC_AUTH_002, TC_AUTH_004 | Đã bao phủ |
| **R3** | Mật khẩu tối thiểu 8 ký tự | TC_AUTH_003, TC_AUTH_014 | Đã bao phủ |
| **R4** | Đăng nhập thành công với thông tin hợp lệ | TC_AUTH_006, TC_AUTH_011 | Đã bao phủ |
| **R5** | Đăng nhập thất bại khi sai mật khẩu | TC_AUTH_007, TC_AUTH_008, TC_AUTH_013 | Đã bao phủ |
| **R6** | Quên mật khẩu gửi email đặt lại | TC_AUTH_009, TC_AUTH_010 | Đã bao phủ |
| **R7** | Tìm kiếm hiển thị đúng kết quả | TC_PROD_001, TC_PROD_002, TC_CART_019 | Đã bao phủ |
| **R8** | Lọc theo giá hoạt động đúng | TC_PROD_003, TC_PROD_001 | Đã bao phủ |
| **R9** | Xem chi tiết sản phẩm | TC_PROD_004, TC_PROD_005 | Đã bao phủ |
| **R10** | Thêm sản phẩm vào giỏ thành công | TC_PROD_006, TC_PROD_007, TC_PROD_008, TC_CART_020 | Đã bao phủ |
| **R11** | Cập nhật số lượng trong giỏ | TC_CART_010, TC_CART_011, TC_CART_012, TC_CART_017 | Đã bao phủ |
| **R12** | Xoá sản phẩm khỏi giỏ | TC_CART_013, TC_CART_014 | Đã bao phủ |
| **R13** | Thanh toán bắt buộc nhập địa chỉ | TC_CHK_003, TC_CHK_001 | Đã bao phủ |
| **R14** | Chọn phương thức thanh toán | TC_CHK_002, TC_CHK_004, TC_CHK_005 | Đã bao phủ |
| **R15** | Đặt hàng thành công | TC_CHK_002, TC_CHK_004, TC_CHK_010 | Đã bao phủ |
| **R16** | Lưu lịch sử đơn hàng | TC_CHK_007, TC_CHK_008, TC_CHK_006 | Đã bao phủ |

**Tổng kết**:
*   Tổng số yêu cầu: 16
*   Số yêu cầu đã được bao phủ: 16
*   Tỷ lệ bao phủ: 100%

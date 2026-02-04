# Ma trận truy vết yêu cầu (Requirement Traceability Matrix - RTM)

| Req ID | Yêu cầu (Requirement) | Test Case ID (Mapping) | Trạng thái Coverage |
| :--- | :--- | :--- | :--- |
| **R1** | Người dùng đăng ký bằng email hợp lệ | TC_AUTH_001, TC_AUTH_014, TC_AUTH_005 | Covered |
| **R2** | Không cho đăng ký khi email sai định dạng | TC_AUTH_002, TC_AUTH_004 | Covered |
| **R3** | Mật khẩu tối thiểu 8 ký tự | TC_AUTH_003, TC_AUTH_014 | Covered |
| **R4** | Đăng nhập thành công với thông tin hợp lệ | TC_AUTH_006, TC_AUTH_011 | Covered |
| **R5** | Đăng nhập thất bại khi sai mật khẩu | TC_AUTH_007, TC_AUTH_008, TC_AUTH_013 | Covered |
| **R6** | Quên mật khẩu gửi email đặt lại | TC_AUTH_009, TC_AUTH_010 | Covered |
| **R7** | Tìm kiếm hiển thị đúng kết quả | TC_PROD_001, TC_PROD_002, TC_CART_019 | Covered |
| **R8** | Lọc theo giá hoạt động đúng | TC_PROD_003, TC_PROD_001 | Covered |
| **R9** | Xem chi tiết sản phẩm | TC_PROD_004, TC_PROD_005 | Covered |
| **R10** | Thêm sản phẩm vào giỏ thành công | TC_PROD_006, TC_PROD_007, TC_PROD_008, TC_CART_020 | Covered |
| **R11** | Cập nhật số lượng trong giỏ | TC_CART_010, TC_CART_011, TC_CART_012, TC_CART_017 | Covered |
| **R12** | Xoá sản phẩm khỏi giỏ | TC_CART_013, TC_CART_014 | Covered |
| **R13** | Thanh toán bắt buộc nhập địa chỉ | TC_CHK_003, TC_CHK_001 | Covered |
| **R14** | Chọn phương thức thanh toán | TC_CHK_002, TC_CHK_004, TC_CHK_005 | Covered |
| **R15** | Đặt hàng thành công | TC_CHK_002, TC_CHK_004, TC_CHK_010 | Covered |
| **R16** | Lưu lịch sử đơn hàng | TC_CHK_007, TC_CHK_008, TC_CHK_006 | Covered |

**Tổng kết**:
*   Tổng số yêu cầu (Requirements): 16
*   Số yêu cầu đã được bao phủ (Covered): 16
*   Tỷ lệ bao phủ (Coverage Rate): 100%

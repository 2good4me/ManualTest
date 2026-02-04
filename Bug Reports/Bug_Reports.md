# Báo cáo lỗi (Bug Reports)

| Bug ID | Tóm tắt (Summary) | Các bước tái hiện (Steps) | Kết quả mong đợi (Expected) | Kết quả thực tế (Actual) | Severity | Priority |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **BUG_CART_001** | Tổng tiền giỏ hàng tính sai khi số lượng > 10 | 1. Thêm SP A (giá 100k) vào giỏ<br>2. Cập nhật số lượng lên 11 | Tổng = 1.100.000đ | Tổng hiển thị = 100.000đ (mất số hàng triệu) | **Critical** | High |
| **BUG_CHK_002** | Không thể hoàn tất đơn hàng khi chọn Visa | 1. Vào trang Checkout<br>2. Chọn Visa<br>3. Nhập thẻ đúng<br>4. Click Đặt hàng | Thông báo thành công | Nút xoay loading mãi mãi, không phản hồi (Time out) | **Critical** | High |
| **BUG_AUTH_003** | Đăng ký thành công với Email thiếu đuôi domain | 1. Nhập email "user@gmail"<br>2. Nhập pass<br>3. Submit | Báo lỗi định dạng email | Tạo tài khoản thành công | Major | High |
| **BUG_PROD_004** | Bộ lọc giá không hoạt động chính xác | 1. Chọn lọc giá 1tr-2tr<br>2. Click Lọc | Chỉ hiện SP 1tr-2tr | Hiển thị cả SP 500k và 5tr | Major | Medium |
| **BUG_CART_005** | Nút "Xóa" sản phẩm trong giỏ hàng thỉnh thoảng không nhận | 1. Vào giỏ hàng<br>2. Click icon thùng rác | Sản phẩm biến mất | Không có phản hồi gì, phải refresh mới mất | Major | Medium |
| **BUG_AUTH_006** | Email quên mật khẩu không được gửi | 1. Chọn Quên mật khẩu<br>2. Nhập email đúng<br>3. Gửi | Nhận được email reset | Không nhận được email nào sau 1 tiếng | Major | High |
| **BUG_UI_007** | Sai chính tả tại footer trang chủ | 1. Scroll xuống footer<br>2. Đọc text bản quyền | "Copyright 2026" | Hiển thị "Copyright 2025" (Sai năm) | Minor | Low |
| **BUG_UI_008** | Mất icon tại nút "Tìm kiếm" trên mobile | 1. Mở web trên Mobile view<br>2. Kiểm tra thanh search | Hiển thị icon kính lúp | Icon bị vỡ hình (ô vuông) | Minor | Low |
| **BUG_PROD_009** | Ảnh sản phẩm bị méo khi xem chi tiết | 1. Vào trang chi tiết SP<br>2. Nhìn ảnh đại diện | Ảnh tỷ lệ chuẩn | Ảnh bị kéo giãn chiều ngang (stretch) | Minor | Low |
| **BUG_CHK_010** | Tab order tại form địa chỉ không theo thứ tự | 1. Click vào ô Họ tên<br>2. Nhấn phím Tab | Chuyển sang ô Số điện thoại | Nhảy xuống footer rồi mới quay lại ô SĐT | Minor | Low |

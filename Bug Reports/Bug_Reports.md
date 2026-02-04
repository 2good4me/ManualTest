# Báo cáo lỗi (Bug Reports)

| Mã Lỗi | Tóm tắt | Các bước tái hiện | Kết quả mong đợi | Kết quả thực tế | Mức độ nghiêm trọng | Độ ưu tiên | Môi trường |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **BUG_CART_001** | Tổng tiền giỏ hàng tính sai khi số lượng > 10 | 1. Thêm SP A (giá 100k) vào giỏ<br>2. Cập nhật số lượng lên 11 | Tổng = 1.100.000đ | Tổng hiển thị = 100.000đ (mất số hàng triệu) | **Nghiêm trọng** | Cao | Windows 10, Chrome 120 |
| **BUG_CHK_002** | Không thể hoàn tất đơn hàng khi chọn Visa | 1. Vào trang Thanh toán<br>2. Chọn Visa<br>3. Nhập thẻ đúng<br>4. Nhấn Đặt hàng | Thông báo thành công | Nút xoay loading mãi mãi, không phản hồi (Time out) | **Nghiêm trọng** | Cao | Windows 11, Chrome 120 |
| **BUG_AUTH_003** | Đăng ký thành công với Email thiếu đuôi tên miền | 1. Nhập email "user@gmail"<br>2. Nhập mật khẩu<br>3. Gửi | Báo lỗi định dạng email | Tạo tài khoản thành công | Lớn (Major) | Cao | Windows 10, Firefox |
| **BUG_PROD_004** | Bộ lọc giá không hoạt động chính xác | 1. Chọn lọc giá 1tr-2tr<br>2. Nhấn Lọc | Chỉ hiện SP 1tr-2tr | Hiển thị cả SP 500k và 5tr | Lớn (Major) | Trung bình | Windows 10, Chrome |
| **BUG_CART_005** | Nút "Xóa" sản phẩm trong giỏ hàng thỉnh thoảng không nhận | 1. Vào giỏ hàng<br>2. Nhấn biểu tượng thùng rác | Sản phẩm biến mất | Không có phản hồi gì, phải tải lại trang mới mất | Lớn (Major) | Trung bình | MacOS, Safari 17 |
| **BUG_AUTH_006** | Email quên mật khẩu không được gửi | 1. Chọn Quên mật khẩu<br>2. Nhập email đúng<br>3. Gửi | Nhận được email đặt lại | Không nhận được email nào sau 1 tiếng | Lớn (Major) | Cao | All Browsers |
| **BUG_UI_007** | Sai chính tả tại chân trang (footer) | 1. Cuộn xuống chân trang<br>2. Đọc văn bản bản quyền | "Copyright 2026" | Hiển thị "Copyright 2025" (Sai năm) | Nhỏ (Minor) | Thấp | All Browsers |
| **BUG_UI_008** | Mất biểu tượng tại nút "Tìm kiếm" trên điện thoại | 1. Mở web trên giao diện điện thoại<br>2. Kiểm tra thanh tìm kiếm | Hiển thị biểu tượng kính lúp | Biểu tượng bị vỡ hình (ô vuông) | Nhỏ (Minor) | Thấp | iPhone 14, Safari |
| **BUG_PROD_009** | Ảnh sản phẩm bị méo khi xem chi tiết | 1. Vào trang chi tiết SP<br>2. Nhìn ảnh đại diện | Ảnh tỷ lệ chuẩn | Ảnh bị kéo giãn chiều ngang | Nhỏ (Minor) | Thấp | Windows 10, Chrome |
| **BUG_CHK_010** | Thứ tự Tab tại form địa chỉ không đúng | 1. Nhấn vào ô Họ tên<br>2. Nhấn phím Tab | Chuyển sang ô Số điện thoại | Nhảy xuống chân trang rồi mới quay lại ô SĐT | Nhỏ (Minor) | Thấp | Windows 10, Edge |

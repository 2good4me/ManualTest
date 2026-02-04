# Test Cases - Checkout Module

| TC ID | Title | Precondition | Steps | Expected Result | Priority | Type |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **TC_CHK_001** | Truy cập trang thanh toán - Giỏ hàng trống | Giỏ hàng rỗng | 1. Click button "Thanh toán" | Hệ thống chặn, yêu cầu mua hàng trước | Medium | Negative |
| **TC_CHK_002** | Thanh toán thành công - COD | Giỏ có hàng, đã login | 1. Nhập địa chỉ<br>2. Chọn COD (Tiền mặt)<br>3. Click "Đặt hàng" | Thông báo đặt hàng thành công, tạo Mã đơn hàng | Critical | Positive |
| **TC_CHK_003** | Thanh toán - Bỏ trống địa chỉ | Tại trang Checkout | 1. Xóa trống địa chỉ<br>2. Click "Đặt hàng" | Báo lỗi bắt buộc nhập địa chỉ | High | Negative |
| **TC_CHK_004** | Thanh toán - Chọn phương thức Visa giả lập | Giỏ có hàng | 1. Nhập địa chỉ<br>2. Chọn Visa<br>3. Nhập thẻ test 4242...<br>4. Đặt hàng | Thanh toán thành công | High | Positive |
| **TC_CHK_005** | Thanh toán - Thẻ Visa hết hạn/sai | Giỏ có hàng | 1. Chọn Visa<br>2. Nhập thẻ sai<br>3. Đặt hàng | Báo lỗi giao dịch thất bại | Medium | Negative |
| **TC_CHK_006** | Hủy đơn hàng (nếu có chức năng) | Đã đặt hàng thành công | 1. Vào Lịch sử đơn hàng<br>2. Chọn đơn "Chờ xử lý"<br>3. Click Hủy | Trạng thái đơn đổi sang "Đã hủy" | Medium | Positive |
| **TC_CHK_007** | Kiểm tra lịch sử đơn hàng | Đã mua hàng | 1. Vào trang cá nhân -> Lịch sử | Danh sách đơn hàng hiển thị đúng ngày, tổng tiền | High | Positive |
| **TC_CHK_008** | Xem chi tiết đơn hàng lịch sử | Tại list đơn hàng | 1. Click vào mã đơn | Hiển thị chi tiết SP đã mua trong đơn đó | Low | Positive |
| **TC_CHK_009** | Kiểm tra phí vận chuyển (Shipping fee) | Trang checkout | 1. Chọn Tỉnh/Thành A<br>2. Chọn Tỉnh/Thành B | Phí ship thay đổi tương ứng (nếu có) | Medium | Positive |
| **TC_CHK_010** | Thanh toán khi Session hết hạn | Đang ở trang Checkout | 1. Chờ session timeout<br>2. Click "Đặt hàng" | Chuyển hướng về trang Login, không tạo đơn hàng rác | High | Security |

# Ca Kiểm Thử - Module Thanh toán

| Mã TC | Tiêu đề | Điều kiện trước | Các bước thực hiện | Kết quả mong đợi | Độ ưu tiên | Loại |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **TC_CHK_001** | Truy cập trang thanh toán - Giỏ hàng trống | Giỏ hàng rỗng | 1. Nhấn nút "Thanh toán" | Hệ thống chặn, yêu cầu mua hàng trước | Trung bình | Không hợp lệ |
| **TC_CHK_002** | Thanh toán thành công - COD | Giỏ có hàng, đã đăng nhập | 1. Nhập địa chỉ<br>2. Chọn COD (Tiền mặt)<br>3. Nhấn "Đặt hàng" | Thông báo đặt hàng thành công, tạo Mã đơn hàng | Nghiêm trọng | Hợp lệ |
| **TC_CHK_003** | Thanh toán - Bỏ trống địa chỉ | Tại trang Thanh toán | 1. Xóa trống địa chỉ<br>2. Nhấn "Đặt hàng" | Báo lỗi bắt buộc nhập địa chỉ | Cao | Không hợp lệ |
| **TC_CHK_004** | Thanh toán - Chọn phương thức Visa giả lập | Giỏ có hàng | 1. Nhập địa chỉ<br>2. Chọn Visa<br>3. Nhập thẻ test 4242...<br>4. Đặt hàng | Thanh toán thành công | Cao | Hợp lệ |
| **TC_CHK_005** | Thanh toán - Thẻ Visa hết hạn/sai | Giỏ có hàng | 1. Chọn Visa<br>2. Nhập thẻ sai<br>3. Đặt hàng | Báo lỗi giao dịch thất bại | Trung bình | Không hợp lệ |
| **TC_CHK_006** | Hủy đơn hàng (nếu có chức năng) | Đã đặt hàng thành công | 1. Vào Lịch sử đơn hàng<br>2. Chọn đơn "Chờ xử lý"<br>3. Nhấn Hủy | Trạng thái đơn đổi sang "Đã hủy" | Trung bình | Hợp lệ |
| **TC_CHK_007** | Kiểm tra lịch sử đơn hàng | Đã mua hàng | 1. Vào trang cá nhân -> Lịch sử | Danh sách đơn hàng hiển thị đúng ngày, tổng tiền | Cao | Hợp lệ |
| **TC_CHK_008** | Xem chi tiết đơn hàng lịch sử | Tại danh sách đơn hàng | 1. Nhấn vào mã đơn | Hiển thị chi tiết SP đã mua trong đơn đó | Thấp | Hợp lệ |
| **TC_CHK_009** | Kiểm tra phí vận chuyển | Trang thanh toán | 1. Chọn Tỉnh/Thành A<br>2. Chọn Tỉnh/Thành B | Phí vận chuyển thay đổi tương ứng (nếu có) | Trung bình | Hợp lệ |
| **TC_CHK_010** | Thanh toán khi Phiên làm việc hết hạn | Đang ở trang Thanh toán | 1. Chờ hết phiên (session timeout)<br>2. Nhấn "Đặt hàng" | Chuyển hướng về trang Đăng nhập, không tạo đơn hàng rác | Cao | Bảo mật |

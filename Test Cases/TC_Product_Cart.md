# Ca Kiểm Thử - Module Sản phẩm & Giỏ hàng

| Mã TC | Tiêu đề | Điều kiện trước | Các bước thực hiện | Kết quả mong đợi | Độ ưu tiên | Loại |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **TC_PROD_001** | Tìm kiếm sản phẩm tồn tại | Tại trang chủ | 1. Nhập từ khóa "Samsung"<br>2. Nhấn Enter | Hiển thị danh sách sản phẩm có tên chứa "Samsung" | Cao | Hợp lệ |
| **TC_PROD_002** | Tìm kiếm sản phẩm không tồn tại | Tại trang chủ | 1. Nhập "xyzabc"<br>2. Nhấn Enter | Hiển thị thông báo "Không tìm thấy sản phẩm" | Trung bình | Không hợp lệ |
| **TC_PROD_003** | Lọc sản phẩm theo khoảng giá | Tại trang danh sách | 1. Chọn khoảng giá 5tr - 10tr<br>2. Nhấn Lọc | Chỉ hiển thị các sản phẩm trong khoảng giá 5tr-10tr | Cao | Hợp lệ |
| **TC_PROD_004** | Xem chi tiết sản phẩm | Tại trang danh sách | 1. Nhấn vào hình ảnh sản phẩm A | Chuyển đến trang chi tiết SP A, hiển thị đúng giá, mô tả | Cao | Hợp lệ |
| **TC_PROD_005** | Kiểm tra hình ảnh sản phẩm (Phóng to) | Tại trang chi tiết | 1. Di chuột vào ảnh chính | Hình ảnh phóng to, rõ nét | Thấp | Giao diện |
| **TC_PROD_006** | Thêm vào giỏ - Hàng còn trong kho | Trang chi tiết SP (còn hàng) | 1. Chọn số lượng 1<br>2. Nhấn "Thêm vào giỏ" | Thông báo thành công, biểu tượng giỏ hàng tăng số lượng lên 1 | Nghiêm trọng | Hợp lệ |
| **TC_PROD_007** | Thêm vào giỏ - Hàng hết kho | Trang chi tiết SP (hết hàng) | 1. Kiểm tra nút "Thêm vào giỏ" | Nút bị vô hiệu hóa hoặc hiển thị "Hết hàng" | Cao | Không hợp lệ |
| **TC_PROD_008** | Thêm vào giỏ - Số lượng tối đa | Trang chi tiết SP (Kho còn 5) | 1. Nhập số lượng 6<br>2. Nhấn "Thêm vào giỏ" | Báo lỗi không đủ số lượng trong kho | Trung bình | Không hợp lệ |
| **TC_CART_009** | Xem giỏ hàng | Giỏ hàng có sản phẩm | 1. Nhấn biểu tượng Giỏ hàng | Hiển thị đúng danh sách SP, đơn giá, tổng tiền tạm tính | Cao | Hợp lệ |
| **TC_CART_010** | Cập nhật số lượng - Tăng | Tại giỏ hàng | 1. Nhấn nút (+) tại SP A | Số lượng tăng lên 1, tổng tiền cập nhật đúng | Cao | Hợp lệ |
| **TC_CART_011** | Cập nhật số lượng - Giảm | Tại giỏ hàng | 1. Nhấn nút (-) tại SP A (đang SL 2) | Số lượng giảm còn 1, tổng tiền cập nhật đúng | Cao | Hợp lệ |
| **TC_CART_012** | Cập nhật số lượng - Nhập số âm | Tại giỏ hàng | 1. Nhập "-1" vào ô số lượng | Hệ thống tự đặt lại về 1 hoặc báo lỗi | Trung bình | Không hợp lệ |
| **TC_CART_013** | Xóa sản phẩm khỏi giỏ | Tại giỏ hàng | 1. Nhấn nút "Xóa" (Biểu tượng thùng rác) | SP bị loại bỏ khỏi danh sách, tổng tiền cập nhật lại | Cao | Hợp lệ |
| **TC_CART_014** | Xóa toàn bộ giỏ hàng | Giỏ hàng có nhiều SP | 1. Nhấn "Xóa tất cả" | Giỏ hàng trống, hiển thị thông báo "Chưa có sản phẩm" | Trung bình | Hợp lệ |
| **TC_CART_015** | Kiểm tra tổng tiền | Giỏ có 2 SP (Giá A, Giá B) | 1. Tính tay: (A*sl) + (B*sl)<br>2. So sánh với hệ thống | Tổng tiền trên giao diện khớp với tính toán | Nghiêm trọng | Hợp lệ |
| **TC_CART_016** | Tiếp tục mua sắm từ giỏ hàng | Tại giỏ hàng | 1. Nhấn "Tiếp tục mua sắm" | Quay lại trang sản phẩm trước đó hoặc trang chủ | Thấp | Hợp lệ |
| **TC_CART_017** | Thêm sản phẩm cùng loại vào giỏ | Giỏ đã có SP A (SL 1) | 1. Vào trang chi tiết SP A<br>2. Thêm tiếp SL 2<br>3. Vào giỏ hàng kiểm tra | SP A không bị tách dòng, số lượng cập nhật thành 3 | Trung bình | Hợp lệ |
| **TC_CART_018** | Kiểm tra lưu giỏ hàng (Sau khi Đăng nhập) | Chưa đăng nhập, thêm hàng vào giỏ | 1. Đăng nhập tài khoản<br>2. Kiểm tra giỏ hàng | Giỏ hàng được đồng bộ (Gộp) với tài khoản | Trung bình | Hợp lệ |
| **TC_CART_019** | Kiểm tra nhập ký tự đặc biệt ô tìm kiếm | Trang chủ | 1. Nhập "%$#@" vào ô tìm kiếm<br>2. Enter | Hệ thống xử lý an toàn, không lỗi crash (Kiểm tra SQLi cơ bản) | Thấp | Bảo mật |
| **TC_CART_020** | Kiểm tra biên giá trị - Số lượng 999 | Trang chi tiết | 1. Nhập 999<br>2. Thêm giỏ | Hệ thống cho phép hoặc báo giới hạn (tùy nghiệp vụ) - Kiểm tra biên | Thấp | Giá trị biên |

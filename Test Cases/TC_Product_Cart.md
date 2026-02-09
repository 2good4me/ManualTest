# Ca Kiểm Thử - Module Sản phẩm & Giỏ hàng
**Website**: https://www.saucedemo.com

| Mã TC | Tiêu đề | Điều kiện trước | Các bước thực hiện | Kết quả mong đợi | Độ ưu tiên | Loại |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **TC_PROD_001** | Xem danh sách Inventory | Đã Login (standard_user) | 1. Quan sát trang Inventory | Hiển thị 6 sản phẩm mặc định (Backpack, Bike Light...) | Cao | Hợp lệ |
| **TC_PROD_002** | Sắp xếp sản phẩm: Review Z to A | Trang Inventory | 1. Nhấn Dropdown Sort<br>2. Chọn "Name (Z to A)" | Sản phẩm đầu tiên là "Test.allTheThings() T-Shirt (Red)" | Cao | Hợp lệ |
| **TC_PROD_003** | Sắp xếp sản phẩm: Price Low to High | Trang Inventory | 1. Nhấn Dropdown Sort<br>2. Chọn "Price (low to high)" | Sản phẩm đầu tiên là "Sauce Labs Onesie" ($7.99) | Cao | Hợp lệ |
| **TC_PROD_004** | Xem chi tiết sản phẩm | Trang Inventory | 1. Nhấn vào tên "Sauce Labs Backpack" | Chuyển đến trang chi tiết, hiển thị đúng giá $29.99 và mô tả | Cao | Hợp lệ |
| **TC_PROD_005** | Quay lại từ trang chi tiết (Back to products) | Trang Chi tiết SP | 1. Nhấn nút "Back to products" | Quay lại trang Inventory chính | Thấp | Điều hướng |
| **TC_PROD_006** | Thêm sản phẩm vào giỏ (Từ Inventory) | Trang Inventory | 1. Nhấn "Add to cart" tại Backpack | Nút đổi thành "Remove", Cart Badge (số trên giỏ) hiện số 1 | Nghiêm trọng | Hợp lệ |
| **TC_PROD_007** | Thêm sản phẩm vào giỏ (Từ Chi tiết) | Trang Chi tiết SP | 1. Nhấn "Add to cart" | Nút đổi thành "Remove", Cart Badge tăng lên | Cao | Hợp lệ |
| **TC_PROD_008** | Xóa sản phẩm khỏi giỏ (Từ Inventory) | Đã thêm SP | 1. Nhấn nút "Remove" tại sản phẩm đã thêm | Nút đổi lại thành "Add to cart", Cart Badge giảm xuống | Cao | Hợp lệ |
| **TC_CART_009** | Vào xem giỏ hàng | Có SP trong giỏ | 1. Nhấn icon Giỏ hàng (góc phải trên) | Vào trang `/cart.html`, hiển thị đúng danh sách SP | Cao | Hợp lệ |
| **TC_CART_010** | Xóa sản phẩm trong trang Cart | Tại trang Cart | 1. Nhấn nút "Remove" bên cạnh SP | Sản phẩm biến mất khỏi danh sách | Cao | Hợp lệ |
| **TC_CART_011** | Tiếp tục mua sắm (Continue Shopping) | Tại trang Cart | 1. Nhấn nút "Continue Shopping" | Quay lại trang Inventory | Thấp | Điều hướng |
| **TC_CART_012** | Kiểm tra hiển thị Product Image (Problem User) | Login bằng `problem_user` | 1. Quan sát ảnh sản phẩm "Sauce Labs Backpack" | Ảnh hiển thị lỗi (Hình con chó) thay vì ảnh Balo | Trung bình | Kịch bản lỗi |
| **TC_CART_013** | Thêm nhiều sản phẩm vào giỏ | Trang Inventory | 1. Add Backpack<br>2. Add Bike Light<br>3. Add Bolt T-Shirt | Cart Badge hiển thị số 3 | Trung bình | Hợp lệ |
| **TC_CART_014** | Giỏ hàng giữ nguyên sau khi Logout/Login | Đã thêm 2 SP | 1. Logout<br>2. Login lại `standard_user` | Giỏ hàng vẫn còn lưu 2 SP đó (Cookie/Session save) | Trung bình | Hợp lệ |
| **TC_CART_015** | Nút Add to Cart không hoạt động (Error User) | Login bằng `error_user` | 1. Nhấn "Add to cart" tại Sauce Labs Fleece | Nút KHÔNG đổi sang "Remove" (Do JS lỗi) hoặc không thêm được | Trung bình | Kịch bản lỗi |
| **TC_CART_016** | Kiểm tra Reset App State | Đã thêm SP | 1. Mở Menu<br>2. Chọn "Reset App State"<br>3. Refresh trang | Giỏ hàng trở về 0, các nút Remove trở về Add to cart | Thấp | Chức năng |
| **TC_CART_017** | Kiểm tra Footer | Footer | 1. Kiểm tra các link Twitter, Facebook, LinkedIn | Các link tồn tại và trỏ đúng địa chỉ Sauce Labs | Thấp | Giao diện |
| **TC_CART_018** | Kiểm tra CSS/Layout khi tên SP dài | Trang Inventory | 1. Quan sát SP "Test.allTheThings() T-Shirt (Red)" | Tên hiển thị đầy đủ, không bị cắt bớt hay vỡ khung | Thấp | Giao diện |
| **TC_CART_019** | Sort ngược Z-A | Trang Inventory | 1. Sort Z-A | Kiểm tra thứ tự và hiển thị | Trung bình | Hợp lệ |
| **TC_CART_020** | Thêm sản phẩm rồi xóa ngay | Trang Inventory | 1. Add to cart<br>2. Remove (ngay lập tức) | Trạng thái nút cập nhật tức thì, không cần refresh | Thấp | UI/UX |

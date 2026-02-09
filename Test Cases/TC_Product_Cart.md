# Ca Kiểm Thử - Module Sản phẩm & Giỏ hàng
**Website**: https://automationexercise.com

| Mã TC | Tiêu đề | Điều kiện trước | Các bước thực hiện | Kết quả mong đợi | Độ ưu tiên | Loại |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **TC_PROD_001** | Xem danh sách sản phẩm | Trang chủ | 1. Nhấn menu "Products" | Chuyển đến trang `/products`, hiển thị danh sách "ALL PRODUCTS" | Cao | Hợp lệ |
| **TC_PROD_002** | Xem chi tiết sản phẩm | Trang Products | 1. Nhấn "View Product" tại SP đầu tiên | Chuyển trang Product Detail, hiển thị: Tên, Giá, Availability, Condition, Brand | Cao | Hợp lệ |
| **TC_PROD_003** | Tìm kiếm sản phẩm | Trang Products | 1. Nhập "Dress" vào ô Search Product<br>2. Nhấn biểu tượng kính lúp | Hiển thị danh sách "SEARCHED PRODUCTS" chứa từ khóa "Dress" | Cao | Hợp lệ |
| **TC_PROD_004** | Tìm kiếm sản phẩm không có kết quả | Trang Products | 1. Nhập "khongtimthay123"<br>2. Nhấn tìm kiếm | Danh sách trống hoặc không hiển thị sản phẩm nào (Không có thông báo lỗi) | Trung bình | Không hợp lệ |
| **TC_PROD_005** | Thêm 1 sản phẩm vào giỏ (Từ trang chủ) | Trang chủ | 1. Hover vào sản phẩm đầu tiên<br>2. Nhấn "Add to cart" | Hiển thị Popup "Added!", nút "View Cart" và "Continue Shopping" | Nghiêm trọng | Hợp lệ |
| **TC_PROD_006** | Thêm sản phẩm vào giỏ (Từ trang chi tiết) | Trang chi tiết SP | 1. Nhập Quantity = 3<br>2. Nhấn "Add to cart" | Hiển thị Popup xác nhận thêm thành công | Cao | Hợp lệ |
| **TC_PROD_007** | Xác minh sản phẩm trong giỏ hàng | Đã thêm SP | 1. Nhấn menu "Cart" hoặc link "View Cart" trên popup | Vào trang `/view_cart`. Hiển thị đúng: Hình ảnh, Tên, Giá, Số lượng, Tổng tiền | Nghiêm trọng | Hợp lệ |
| **TC_CART_008** | Xóa sản phẩm khỏi giỏ | Giỏ hàng có SP | 1. Nhấn nút "X" (Delete) bên cạnh sản phẩm | Sản phẩm biến mất khỏi danh sách ngay lập tức | Cao | Hợp lệ |
| **TC_CART_009** | Thêm sản phẩm cùng loại (Cộng dồn) | Giỏ đã có SP A (SL 1) | 1. Thêm tiếp SP A với SL 1 nữa<br>2. Vào Cart kiểm tra | SP A hiển thị 1 dòng với SL = 2 | Trung bình | Hợp lệ |
| **TC_CART_010** | Lọc sản phẩm theo Category (Women - Dress) | Trang Products | 1. Sidebar trái: Nhấn "Women"<br>2. Nhấn "Dress" | Hiển thị danh sách "WOMEN - DRESS PRODUCTS" | Trung bình | Hợp lệ |
| **TC_CART_011** | Lọc sản phẩm theo Brand (Polo) | Trang Products | 1. Sidebar trái: Mục Brands, nhấn "Polo" | Hiển thị danh sách sản phẩm thương hiệu Polo | Trung bình | Hợp lệ |
| **TC_CART_012** | Review sản phẩm (Viết đánh giá) | Trang chi tiết SP | 1. Nhập Name, Email<br>2. Viết Review<br>3. Nhấn Submit | Thông báo "Thank you for your review." | Thấp | Hợp lệ |
| **TC_CART_013** | Review sản phẩm - Thiếu thông tin | Trang chi tiết SP | 1. Bỏ trống Name/Email<br>2. Nhấn Submit | Trình duyệt báo lỗi tại ô Name/Email: "Please fill out this field" | Thấp | Không hợp lệ |
| **TC_CART_014** | Kiểm tra hiển thị Recommended Items | Footer trang chủ | 1. Cuộn xuống dưới cùng<br>2. Xem phần "RECOMMENDED ITEMS" | Slider hoạt động, có thể add to cart từ đây | Thấp | Giao diện |
| **TC_CART_015** | Đăng ký khi đang Checkout (Luồng kết hợp) | Giỏ có hàng, chưa login | 1. Vào Cart -> Proceed to Checkout<br>2. Popup yêu cầu Login -> Nhấn "Register / Login"<br>3. Tạo tài khoản mới | Sau khi tạo xong, nhấn Cart -> Checkout, hệ thống cho phép tiếp tục | Cao | Hợp lệ |
| **TC_CART_016** | Kiểm tra tính đúng đắn của giá (Total Price) | Giỏ hàng | 1. Kiểm tra: Price * Quantity = Total | Phép tính đúng cho từng dòng sản phẩm | Nghiêm trọng | Hợp lệ |
| **TC_CART_017** | Nhập Quantity số âm hoặc 0 | Trang chi tiết SP | 1. Nhập Quantity = -1<br>2. Add to cart | Hệ thống ghi nhận số lượng là 1 (Web tự xử lý logic) hoặc báo lỗi | Trung bình | Giá trị biên |
| **TC_CART_018** | Thêm sản phẩm vào giỏ hàng trống | Giỏ hàng trống | 1. Vào trang Cart | Hiển thị "Cart is empty!" cùng nút "Click here to buy products" | Thấp | Hợp lệ |
| **TC_CART_019** | Kiểm tra điều hướng Breadcrumb | Trang Product Detail | 1. Nhấn vào Home > Product trên breadcrumb | Điều hướng về đúng trang cha | Thấp | Giao diện |
| **TC_CART_020** | Scroll Up / Scroll Down (Mũi tên lên) | Trang chủ | 1. Cuộn xuống cuối<br>2. Nhấn nút mũi tên lên (góc phải) | Trang tự cuộn mượt mà lên đầu trang | Thấp | Giao diện |

# Ca Kiểm Thử - Module Thanh toán
**Website**: https://www.saucedemo.com

| Mã TC | Tiêu đề | Điều kiện trước | Các bước thực hiện | Kết quả mong đợi | Độ ưu tiên | Loại |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **TC_CHK_001** | Checkout thành công (Standard User) | Giỏ có hàng | 1. Checkout<br>2. Điền First/Last Name, Zip<br>3. Continue<br>4. Finish | Chuyển đến trang "Checkout: Complete!" với thông báo "Thank you for your order!" | Nghiêm trọng | Hợp lệ |
| **TC_CHK_002** | Checkout thất bại - Bỏ trống First Name | Trang Checkout: Step 1 | 1. Bỏ trống First Name<br>2. Điền Last Name, Zip<br>3. Continue | Hệ thống báo lỗi: "Error: First Name is required" | Cao | Không hợp lệ |
| **TC_CHK_003** | Checkout thất bại - Bỏ trống Last Name | Trang Checkout: Step 1 | 1. Điền First Name<br>2. Bỏ trống Last Name<br>3. Continue | Hệ thống báo lỗi: "Error: Last Name is required" | Cao | Không hợp lệ |
| **TC_CHK_004** | Checkout thất bại - Bỏ trống Postal Code | Trang Checkout: Step 1 | 1. Điền đủ tên<br>2. Bỏ trống Zip Code<br>3. Continue | Hệ thống báo lỗi: "Error: Postal Code is required" | Cao | Không hợp lệ |
| **TC_CHK_005** | Nhập Last Name dặc biệt (Problem User) | Login `problem_user`, Checkout | 1. Nhập Last Name<br>2. Continue | Hệ thống tự động ghi đè Last Name thành một chuỗi ký tự lạ (Lỗi cố ý của Problem User) | Trung bình | Kịch bản lỗi |
| **TC_CHK_006** | Kiểm tra trang Overview - Tổng tiền | Trang Checkout: Step 2 | 1. Cộng tay: Item Total + Tax<br>2. So sánh với Total hiển thị | Tổng tiền tính toán chính xác (Tax = 8%) | Nghiêm trọng | Hợp lệ |
| **TC_CHK_007** | Kiểm tra danh sách hàng tại Overview | Trang Checkout: Step 2 | 1. Quan sát danh sách sản phẩm | Hiển thị đúng sản phẩm và số lượng đã chọn | Cao | Hợp lệ |
| **TC_CHK_008** | Nút Cancel tại màn hình Information | Trang Checkout: Step 1 | 1. Nhấn "Cancel" | Quay lại trang Cart | Thấp | Điều hướng |
| **TC_CHK_009** | Nút Cancel tại màn hình Overview | Trang Checkout: Step 2 | 1. Nhấn "Cancel" | Quay lại trang Inventory | Thấp | Điều hướng |
| **TC_CHK_010** | Back Home sau khi hoàn tất | Trang Checkout: Complete | 1. Nhấn "Back Home" | Quay lại trang Inventory, Giỏ hàng được làm trống | Trung bình | Điều hướng |

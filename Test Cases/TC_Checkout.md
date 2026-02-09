# Ca Kiểm Thử - Module Thanh toán
**Website**: https://automationexercise.com

| Mã TC | Tiêu đề | Điều kiện trước | Các bước thực hiện | Kết quả mong đợi | Độ ưu tiên | Loại |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **TC_CHK_001** | Thanh toán thành công (Luồng đầy đủ) | Đã Login, Giỏ có hàng | 1. Vào Cart -> Nhấn "Proceed To Checkout"<br>2. Kiểm tra Address & Review Order<br>3. Nhập Comment (nếu cần)<br>4. Nhấn "Place Order"<br>5. Nhập Payment: Name on Card, Card Number, CVC, Expiration<br>6. Nhấn "Pay and Confirm Order" | Thông báo "ORDER PLACED!" / "Congratulations! Your order has been confirmed!" | Nghiêm trọng | Hợp lệ |
| **TC_CHK_002** | Thanh toán khi chưa đăng nhập | Chưa Login, Giỏ có hàng | 1. Vào Cart -> Nhấn "Proceed To Checkout" | Hiển thị Popup "Register / Login" để tiếp tục | Cao | Không hợp lệ |
| **TC_CHK_003** | Kiểm tra thông tin địa chỉ giao hàng | Đã Login | 1. Tại trang Checkout (Review Order)<br>2. So sánh "Delivery Address" với thông tin đã đăng ký | Thông tin (Tên, SĐT, Địa chỉ) khớp chính xác | Cao | Hợp lệ |
| **TC_CHK_004** | Xóa sản phẩm tại bước Review Order | Trang Checkout | 1. Quan sát danh sách sản phẩm<br>2. Quay lại Cart để xóa SP | Hệ thống cập nhật lại danh sách Review Order sau khi xóa | Trung bình | Hợp lệ |
| **TC_CHK_005** | Thanh toán - Bỏ trống thông tin thẻ | Trang Payment | 1. Bỏ trống các trường Card<br>2. Nhấn "Pay and Confirm Order" | Trình duyệt báo lỗi tại ô Name on Card: "Please fill out this field" | Cao | Không hợp lệ |
| **TC_CHK_006** | Tải hóa đơn (Download Invoice) | Sau khi đặt hàng thành công | 1. Tại màn hình "Order Placed"<br>2. Nhấn "Download Invoice" | Tải xuống file hóa đơn (.txt hoặc .pdf) thành công | Trung bình | Hợp lệ |
| **TC_CHK_007** | Tiếp tục mua sắm sau khi thanh toán | Màn hình Order Placed | 1. Nhấn nút "Continue" | Quay về trang chủ để mua sắm tiếp | Thấp | Hợp lệ |
| **TC_CHK_008** | Kiểm tra tổng tiền đơn hàng (Total Amount) | Trang Payment | 1. Kiểm tra số tiền hiển thị "Total Amount" | Phải khớp với Total Amount trong Giỏ hàng trước đó | Nghiêm trọng | Hợp lệ |
| **TC_CHK_009** | Nhập sai định dạng thẻ (Test Validation) | Trang Payment | 1. Nhập Card Number có chữ cái<br>2. Nhấn Pay | Hệ thống báo lỗi hoặc không cho nhập chữ vào ô số (Input type="text" có thể vẫn nhận, đây là test) | Trung bình | Không hợp lệ |
| **TC_CHK_010** | Quay lại (Back) khi đang thanh toán | Trang Payment | 1. Nhấn nút Back của trình duyệt | Quay lại trang Cart hoặc Checkout mà không mất session | Thấp | Giao diện |

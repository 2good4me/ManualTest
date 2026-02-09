# Báo cáo lỗi (Bug Reports)
**Website**: https://www.saucedemo.com

| Mã Lỗi | Tóm tắt | Các bước tái hiện | Kết quả mong đợi | Kết quả thực tế | Mức độ nghiêm trọng | Độ ưu tiên | Môi trường |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **BUG_AUTH_001** | User `locked_out_user` không đăng nhập được | 1. Login user: `locked_out_user`<br>2. Pass: `secret_sauce` | Đăng nhập được (Nếu không biết rules) | Báo lỗi: "Epic sadface: Sorry, this user has been locked out." | Lớn (Major) | Cao | All Browsers |
| **BUG_UI_002** | Ảnh sản phẩm bị lỗi (con chó) với `problem_user` | 1. Login user: `problem_user`<br>2. Xem Inventory | Hiển thị ảnh Balo, Áo đúng | Hiển thị ảnh con chó (Image Link Broken) cho tất cả SP | Lớn (Major) | Cao | All Browsers |
| **BUG_CHK_003** | Không thể nhập Last Name với `problem_user` tại Checkout | 1. Login `problem_user`<br>2. Checkout -> Nhập Last Name "Smith"<br>3. Continue | Last Name là "Smith" | Last Name bị đổi thành ký tự lỗi (Do kịch bản trang web) | Nghiêm trọng | Cao | All Browsers |
| **BUG_PROD_004** | Performance Glitch User load trang chậm | 1. Login `performance_glitch_user` | Vào trang ngay lập tức (<1s) | Load trang mất >4s (Lỗi hiệu năng) | Nhỏ (Minor) | Thấp | Chrome |
| **BUG_CART_005** | `error_user` không thể Remove sản phẩm khỏi giỏ | 1. Login `error_user`<br>2. Add to Cart<br>3. Nhấn Remove | Nút đổi lại Add to cart | Nút không phản hồi (JS Error) | Lớn (Major) | Trung bình | Firefox |
| **BUG_UI_006** | layout bị lệch với `visual_user` | 1. Login `visual_user`<br>2. Xem trang Cart | Nút Checkout thẳng hàng | Nút Checkout bị lệch sang phải, icon giỏ hàng lệch | Nhỏ (Minor) | Thấp | Edge |
| **BUG_CHK_007** | Nhập ký tự đặc biệt vào Zip Code không báo lỗi | 1. Checkout<br>2. Zip Code: "!@#$"<br>3. Continue | Báo lỗi Zip code không hợp lệ | Hệ thống cho qua (Chấp nhận Zip code sai) | Trung bình | Thấp | Chrome |
| **BUG_AUTH_008** | Thông báo lỗi Login không biến mất tự động | 1. Login sai<br>2. Chờ 10s | Thông báo tự ẩn | Thông báo hiển thị mãi nếu không tắt | Nhỏ (Minor) | Thấp | All Browsers |
| **BUG_PROD_009** | Sort Z-A không hoạt động với `problem_user` | 1. Login `problem_user`<br>2. Sort Z-A | Danh sách sắp xếp Z-A | Danh sách không thay đổi (Vẫn A-Z) | Lớn (Major) | Trung bình | Chrome |
| **BUG_CHK_010** | Dữ liệu Overview không khớp với Cart (Simulation) | 1. Add 2 item<br>2. Checkout Overview | Tổng tiền = A + B | Tổng tiền hiển thị sai (Giả lập lỗi logic) | Nghiêm trọng | Cao | Chrome |

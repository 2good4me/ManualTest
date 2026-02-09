# Ca Kiểm Thử - Module Xác thực
**Website**: https://www.saucedemo.com

| Mã TC | Tiêu đề | Điều kiện trước | Các bước thực hiện | Kết quả mong đợi | Độ ưu tiên | Loại |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **TC_AUTH_001** | Đăng nhập thành công (Standard User) | Trang Login | 1. Nhập User: `standard_user`<br>2. Nhập Pass: `secret_sauce`<br>3. Nhấn "Login" | Đăng nhập thành công, chuyển đến trang Inventory (/inventory.html) | Nghiêm trọng | Hợp lệ |
| **TC_AUTH_002** | Đăng nhập thất bại - Bỏ trống Username | Trang Login | 1. Bỏ trống Username & Password<br>2. Nhấn "Login" | Hệ thống báo lỗi: "Epic sadface: Username is required" | Cao | Không hợp lệ |
| **TC_AUTH_003** | Đăng nhập thất bại - Bỏ trống Password | Trang Login | 1. Nhập User: `standard_user`<br>2. Bỏ trống Password<br>3. Nhấn "Login" | Hệ thống báo lỗi: "Epic sadface: Password is required" | Cao | Không hợp lệ |
| **TC_AUTH_004** | Đăng nhập thất bại - Sai Password | Trang Login | 1. Nhập User: `standard_user`<br>2. Nhập Pass: `wrong_pass`<br>3. Nhấn "Login" | Hệ thống báo lỗi: "Epic sadface: Username and password do not match any user in this service" | Cao | Không hợp lệ |
| **TC_AUTH_005** | Đăng nhập thất bại - Tài khoản bị khóa (Locked Out) | Trang Login | 1. Nhập User: `locked_out_user`<br>2. Nhập Pass: `secret_sauce`<br>3. Nhấn "Login" | Hệ thống báo lỗi: "Epic sadface: Sorry, this user has been locked out." | Cao | Không hợp lệ |
| **TC_AUTH_006** | Đăng xuất | Đã đăng nhập | 1. Nhấn Menu (Burger icon)<br>2. Nhấn "Logout" | Đăng xuất thành công, quay về màn hình Login | Cao | Hợp lệ |
| **TC_AUTH_007** | Đăng nhập với Problem User (User lỗi) | Trang Login | 1. Nhập User: `problem_user`<br>2. Nhập Pass: `secret_sauce`<br>3. Nhấn "Login" | Đăng nhập thành công, nhưng hiển thị ảnh sản phẩm bị lỗi (hình con chó) | Trung bình | Hợp lệ |
| **TC_AUTH_008** | Đăng nhập với Performance Glitch User (User lag) | Trang Login | 1. Nhập User: `performance_glitch_user`<br>2. Nhập Pass: `secret_sauce`<br>3. Nhấn "Login" | Đăng nhập thành công, nhưng mất nhiều thời gian hơn bình thường để load trang Inventory (> 3 giây) | Thấp | Hiệu năng |
| **TC_AUTH_009** | Đăng nhập với Error User (User lỗi JS) | Trang Login | 1. Nhập User: `error_user`<br>2. Nhập Pass: `secret_sauce`<br>3. Nhấn "Login" | Đăng nhập thành công, nhưng các thao tác Add to cart có thể bị lỗi | Trung bình | Hợp lệ |
| **TC_AUTH_010** | Đăng nhập với Visual User (User lỗi giao diện) | Trang Login | 1. Nhập User: `visual_user`<br>2. Nhập Pass: `secret_sauce`<br>3. Nhấn "Login" | Đăng nhập thành công, nhưng giao diện (UI) bị vỡ, lệch layout ở một số chỗ | Trung bình | Giao diện |
| **TC_AUTH_011** | Bảo mật - Copy Paste Password | Trang Login | 1. Copy text `secret_sauce`<br>2. Paste vào ô Password | Cho phép paste (hoặc chặn tùy requirement - ở đây web cho phép) | Thấp | Bảo mật |
| **TC_AUTH_012** | Kiểm tra hiển thị Password (Masking) | Trang Login | 1. Nhập password | Ký tự password hiển thị dạng dấu chấm đen (•) | Thấp | Bảo mật |
| **TC_AUTH_013** | Đăng nhập bằng phím Enter | Trang Login | 1. Nhập User & Pass<br>2. Nhấn phím Enter | Đăng nhập thành công (tương đương click nút Login) | Thấp | UI/UX |
| **TC_AUTH_014** | Kiểm tra nút đóng thông báo lỗi | Trang Login | 1. Gây ra lỗi login (để hiện thông báo đỏ)<br>2. Nhấn nút "X" trên thông báo lỗi | Thông báo lỗi biến mất | Thấp | Giao diện |
| **TC_AUTH_015** | Đăng nhập sau khi Logout | Trang Login | 1. Đăng xuất<br>2. Đăng nhập lại ngay lập tức | Đăng nhập thành công bình thường | Trung bình | Hợp lệ |

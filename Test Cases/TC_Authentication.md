# Ca Kiểm Thử - Module Xác thực
**Website**: https://automationexercise.com

| Mã TC | Tiêu đề | Điều kiện trước | Các bước thực hiện | Kết quả mong đợi | Độ ưu tiên | Loại |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **TC_AUTH_001** | Đăng ký thành công | Chưa đăng nhập | 1. Vào trang chủ, nhấn "Signup / Login"<br>2. Tại mục "New User Signup!", nhập Name và Email<br>3. Nhấn "Signup"<br>4. Điền thông tin chi tiết (Title, Password, Date of birth)<br>5. Chọn checkbox "Sign up for our newsletter!"<br>6. Điền thông tin Address<br>7. Nhấn "Create Account" | Hệ thống thông báo "ACCOUNT CREATED!", hiển thị nút "Continue" | Cao | Hợp lệ |
| **TC_AUTH_002** | Đăng ký thất bại - Email đã tồn tại | Email "test@email.com" đã tồn tại | 1. Vào trang "Signup / Login"<br>2. Nhập Name và Email đã tồn tại<br>3. Nhấn "Signup" | Báo lỗi "Email Address already exist!" | Cao | Không hợp lệ |
| **TC_AUTH_003** | Đăng nhập thành công | Đã có tài khoản | 1. Vào trang "Signup / Login"<br>2. Tại mục "Login to your account", nhập Email & Password đúng<br>3. Nhấn "Login" | Đăng nhập thành công, thay đổi menu thành "Logged in as [Username]" | Nghiêm trọng | Hợp lệ |
| **TC_AUTH_004** | Đăng nhập thất bại - Sai mật khẩu | Tài khoản tồn tại | 1. Nhập Email đúng<br>2. Nhập Mật khẩu sai<br>3. Nhấn "Login" | Báo lỗi "incorrect email or password!" | Cao | Không hợp lệ |
| **TC_AUTH_005** | Đăng nhập thất bại - Sai Email | Email chưa đăng ký | 1. Nhập Email chưa đăng ký<br>2. Nhập Mật khẩu bất kỳ<br>3. Nhấn "Login" | Báo lỗi "incorrect email or password!" | Cao | Không hợp lệ |
| **TC_AUTH_006** | Đăng xuất hệ thống | Đang đăng nhập | 1. Nhấn nút "Logout" trên thanh menu | Hệ thống đăng xuất, chuyển hướng về trang Login | Cao | Hợp lệ |
| **TC_AUTH_007** | Đăng ký thất bại - Bỏ trống Email | Trang Signup | 1. Nhập Name<br>2. Bỏ trống Email<br>3. Nhấn Signup | Trình duyệt báo lỗi "Please fill out this field" (HTML5 validation) | Thấp | Không hợp lệ |
| **TC_AUTH_008** | Liên hệ (Contact Us) - Upload file | Tại trang Contact Us | 1. Nhập Name, Email, Subject, Message<br>2. Nhấn "Upload file" và chọn 1 ảnh<br>3. Nhấn Submit | Thông báo "Success! Your details have been submitted successfully." | Trung bình | Hợp lệ |
| **TC_AUTH_009** | Xóa tài khoản (Delete Account) | Đang đăng nhập | 1. Nhấn nút "Delete Account" trên menu | Thông báo "ACCOUNT DELETED!", tài khoản bị xóa khỏi hệ thống | Cao | Hợp lệ |
| **TC_AUTH_010** | Đăng nhập với tài khoản bị xóa | Tài khoản vừa xóa ở TC_009 | 1. Thử đăng nhập lại bằng email vừa xóa | Báo lỗi hoặc không tìm thấy tài khoản | Trung bình | Không hợp lệ |
| **TC_AUTH_011** | Kiểm tra hiển thị giao diện Login | Trang Login | 1. Quan sát bố cục form Login và Signup | Hai form hiển thị song song, rõ ràng, không bị vỡ khung | Thấp | Giao diện |
| **TC_AUTH_012** | Đăng ký - Kiểm tra độ mạnh mật khẩu | Trang nhập thông tin Account | 1. Nhập mật khẩu < 4 ký tự<br>2. Hoàn tất form | Hệ thống có thể cho phép hoặc cảnh báo (Tùy chính sách trang) | Thấp | Bảo mật |
| **TC_AUTH_013** | Đăng nhập - SQL Injection đơn giản | Trang Login | 1. Nhập Email `' OR 1=1 --`<br>2. Nhấn Login | Không đăng nhập được, báo lỗi sai thông tin | Cao | Bảo mật |
| **TC_AUTH_014** | Submit form Signup rỗng | Trang Signup | 1. Không nhập gì<br>2. Nhấn Signup | Trình duyệt báo lỗi "Please fill out this field" (HTML5 validation)| Thấp | Không hợp lệ |
| **TC_AUTH_015** | Subscription (Đăng ký nhận tin) ở Footer | Footer trang chủ | 1. Nhập email vào ô Subscription<br>2. Nhấn mũi tên gửi | Thông báo "You have been successfully subscribed!" | Thấp | Hợp lệ |

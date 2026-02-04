# Test Cases - Authentication Module

| TC ID | Title | Precondition | Steps | Expected Result | Priority | Type |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **TC_AUTH_001** | Đăng ký thành công với thông tin hợp lệ | Người dùng chưa đăng nhập, đang ở trang Đăng ký | 1. Nhập Email hợp lệ<br>2. Nhập Mật khẩu hợp lệ (>=8 ký tự)<br>3. Nhập lại mật khẩu<br>4. Click "Đăng ký" | Hệ thống thông báo tạo tài khoản thành công và chuyển hướng đến trang Login | High | Positive |
| **TC_AUTH_002** | Đăng ký thất bại - Email sai định dạng | Đang ở trang Đăng ký | 1. Nhập Email "user@domain"<br>2. Nhập Pass hợp lệ<br>3. Click "Đăng ký" | Hệ thống báo lỗi định dạng Email không hợp lệ | Medium | Negative |
| **TC_AUTH_003** | Đăng ký thất bại - Mật khẩu < 8 ký tự | Đang ở trang Đăng ký | 1. Nhập Email hợp lệ<br>2. Nhập Pass "1234567"<br>3. Click "Đăng ký" | Hệ thống báo lỗi mật khẩu phải từ 8 ký tự trở lên | Medium | Negative |
| **TC_AUTH_004** | Đăng ký thất bại - Email đã tồn tại | Email "test@demo.com" đã có trong DB | 1. Nhập Email "test@demo.com"<br>2. Nhập Pass hợp lệ<br>3. Click "Đăng ký" | Hệ thống báo lỗi Email đã được sử dụng | High | Negative |
| **TC_AUTH_005** | Đăng ký thất bại - Bỏ trống trường bắt buộc | Đang ở trang Đăng ký | 1. Để trống Email và Pass<br>2. Click "Đăng ký" | Hệ thống hiển thị message yêu cầu nhập thông tin | Low | Negative |
| **TC_AUTH_006** | Đăng nhập thành công | Tài khoản "user1@demo.com" / "Pass1234" tồn tại | 1. Vào trang Login<br>2. Nhập Email "user1@demo.com"<br>3. Nhập Pass "Pass1234"<br>4. Click "Đăng nhập" | Đăng nhập thành công, chuyển về trang chủ | Critical | Positive |
| **TC_AUTH_007** | Đăng nhập thất bại - Sai mật khẩu | Tài khoản tồn tại | 1. Nhập Email đúng<br>2. Nhập Pass sai<br>3. Click "Đăng nhập" | Báo lỗi thông tin đăng nhập không chính xác | High | Negative |
| **TC_AUTH_008** | Đăng nhập thất bại - Email chưa đăng ký | Email chưa có trong hệ thống | 1. Nhập Email chưa tồn tại<br>2. Nhập Pass bất kỳ<br>3. Click "Đăng nhập" | Báo lỗi thông tin đăng nhập không chính xác | High | Negative |
| **TC_AUTH_009** | Quên mật khẩu - Email hợp lệ | Tài khoản tồn tại | 1. Click "Quên mật khẩu"<br>2. Nhập Email đăng ký<br>3. Click "Gửi" | Hệ thống thông báo đã gửi link reset vào email | High | Positive |
| **TC_AUTH_010** | Quên mật khẩu - Email không tồn tại | Email chưa đăng ký | 1. Click "Quên mật khẩu"<br>2. Nhập Email chưa đăng ký<br>3. Click "Gửi" | Hệ thống báo lỗi Email không tồn tại trong hệ thống | Medium | Negative |
| **TC_AUTH_011** | Kiểm tra hiển thị mật khẩu (Show/Hide) | Trang Login | 1. Nhập mật khẩu<br>2. Click icon "Mắt" | Mật khẩu chuyển đổi giữa dạng text và dạng dấu chấm | Low | UI/UX |
| **TC_AUTH_012** | Đăng xuất hệ thống | Người dùng đang đăng nhập | 1. Click Avatar/Menu<br>2. Click "Đăng xuất" | Đăng xuất thành công, quay về trang Login/Home | High | Positive |
| **TC_AUTH_013** | Kiểm tra bảo mật - Login SQL Injection | Trang Login | 1. Nhập Email `' OR 1=1 --`<br>2. Nhập Pass bất kỳ<br>3. Click Login | Hệ thống không cho phép login, báo lỗi sai thông tin | High | Security |
| **TC_AUTH_014** | Kiểm tra biên - Mật khẩu đúng 8 ký tự | Trang Đăng ký | 1. Nhập WebUser<br>2. Nhập Pass "12345678"<br>3. Click Đăng ký | Đăng ký thành công | Medium | Boundary |
| **TC_AUTH_015** | Kiểm tra Session Timeout | Đã đăng nhập | 1. Để màn hình chờ 30 phút<br>2. F5 hoặc thao tác bất kỳ | Hệ thống tự logout hoặc yêu cầu đăng nhập lại | Low | Security |

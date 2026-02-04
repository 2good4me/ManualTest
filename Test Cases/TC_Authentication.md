# Ca Kiểm Thử - Module Xác thực

| Mã TC | Tiêu đề | Điều kiện trước | Các bước thực hiện | Kết quả mong đợi | Độ ưu tiên | Loại |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **TC_AUTH_001** | Đăng ký thành công với thông tin hợp lệ | Người dùng chưa đăng nhập, đang ở trang Đăng ký | 1. Nhập Email hợp lệ<br>2. Nhập Mật khẩu hợp lệ (>=8 ký tự)<br>3. Nhập lại mật khẩu<br>4. Nhấn "Đăng ký" | Hệ thống thông báo tạo tài khoản thành công và chuyển hướng đến trang Đăng nhập | Cao | Hợp lệ |
| **TC_AUTH_002** | Đăng ký thất bại - Email sai định dạng | Đang ở trang Đăng ký | 1. Nhập Email "user@domain"<br>2. Nhập Mật khẩu hợp lệ<br>3. Nhấn "Đăng ký" | Hệ thống báo lỗi định dạng Email không hợp lệ | Trung bình | Không hợp lệ |
| **TC_AUTH_003** | Đăng ký thất bại - Mật khẩu < 8 ký tự | Đang ở trang Đăng ký | 1. Nhập Email hợp lệ<br>2. Nhập Mật khẩu "1234567"<br>3. Nhấn "Đăng ký" | Hệ thống báo lỗi mật khẩu phải từ 8 ký tự trở lên | Trung bình | Không hợp lệ |
| **TC_AUTH_004** | Đăng ký thất bại - Email đã tồn tại | Email "test@demo.com" đã có trong CSDL | 1. Nhập Email "test@demo.com"<br>2. Nhập Mật khẩu hợp lệ<br>3. Nhấn "Đăng ký" | Hệ thống báo lỗi Email đã được sử dụng | Cao | Không hợp lệ |
| **TC_AUTH_005** | Đăng ký thất bại - Bỏ trống trường bắt buộc | Đang ở trang Đăng ký | 1. Để trống Email và Mật khẩu<br>2. Nhấn "Đăng ký" | Hệ thống hiển thị thông báo yêu cầu nhập thông tin | Thấp | Không hợp lệ |
| **TC_AUTH_006** | Đăng nhập thành công | Tài khoản "user1@demo.com" / "Pass1234" tồn tại | 1. Vào trang Đăng nhập<br>2. Nhập Email "user1@demo.com"<br>3. Nhập Mật khẩu "Pass1234"<br>4. Nhấn "Đăng nhập" | Đăng nhập thành công, chuyển về trang chủ | Nghiêm trọng | Hợp lệ |
| **TC_AUTH_007** | Đăng nhập thất bại - Sai mật khẩu | Tài khoản tồn tại | 1. Nhập Email đúng<br>2. Nhập Mật khẩu sai<br>3. Nhấn "Đăng nhập" | Báo lỗi thông tin đăng nhập không chính xác | Cao | Không hợp lệ |
| **TC_AUTH_008** | Đăng nhập thất bại - Email chưa đăng ký | Email chưa có trong hệ thống | 1. Nhập Email chưa tồn tại<br>2. Nhập Mật khẩu bất kỳ<br>3. Nhấn "Đăng nhập" | Báo lỗi thông tin đăng nhập không chính xác | Cao | Không hợp lệ |
| **TC_AUTH_009** | Quên mật khẩu - Email hợp lệ | Tài khoản tồn tại | 1. Nhấn "Quên mật khẩu"<br>2. Nhập Email đăng ký<br>3. Nhấn "Gửi" | Hệ thống thông báo đã gửi liên kết đặt lại vào email | Cao | Hợp lệ |
| **TC_AUTH_010** | Quên mật khẩu - Email không tồn tại | Email chưa đăng ký | 1. Nhấn "Quên mật khẩu"<br>2. Nhập Email chưa đăng ký<br>3. Nhấn "Gửi" | Hệ thống báo lỗi Email không tồn tại trong hệ thống | Trung bình | Không hợp lệ |
| **TC_AUTH_011** | Kiểm tra hiển thị mật khẩu (Ẩn/Hiện) | Trang Đăng nhập | 1. Nhập mật khẩu<br>2. Nhấn biểu tượng "Mắt" | Mật khẩu chuyển đổi giữa dạng văn bản và dạng dấu chấm | Thấp | Giao diện |
| **TC_AUTH_012** | Đăng xuất hệ thống | Người dùng đang đăng nhập | 1. Nhấn Ảnh đại diện/Menu<br>2. Nhấn "Đăng xuất" | Đăng xuất thành công, quay về trang Đăng nhập/Trang chủ | Cao | Hợp lệ |
| **TC_AUTH_013** | Kiểm tra bảo mật - Login SQL Injection | Trang Đăng nhập | 1. Nhập Email `' OR 1=1 --`<br>2. Nhập Mật khẩu bất kỳ<br>3. Nhấn Đăng nhập | Hệ thống không cho phép đăng nhập, báo lỗi sai thông tin | Cao | Bảo mật |
| **TC_AUTH_014** | Kiểm tra biên - Mật khẩu đúng 8 ký tự | Trang Đăng ký | 1. Nhập Tên người dùng<br>2. Nhập Mật khẩu "12345678"<br>3. Nhấn Đăng ký | Đăng ký thành công | Trung bình | Giá trị biên |
| **TC_AUTH_015** | Kiểm tra Hết phiên làm việc (Session Timeout) | Đã đăng nhập | 1. Để màn hình chờ 30 phút<br>2. Tải lại trang hoặc thao tác bất kỳ | Hệ thống tự đăng xuất hoặc yêu cầu đăng nhập lại | Thấp | Bảo mật |

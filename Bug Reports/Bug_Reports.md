# Báo cáo lỗi (Bug Reports)
**Website**: https://automationexercise.com

| Mã Lỗi | Tóm tắt | Các bước tái hiện | Kết quả mong đợi | Kết quả thực tế | Mức độ nghiêm trọng | Độ ưu tiên | Môi trường |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **BUG_AUTH_001** | Login thất bại không xóa mật khẩu cũ | 1. Nhập Email đúng, Pass sai<br>2. Nhấn Login<br>3. Quan sát ô Password | Ô Password nên tự động xóa trống để nhập lại | Ô Password vẫn giữ nguyên ký tự cũ (Rủi ro bảo mật nhẹ) | Nhỏ (Minor) | Thấp | Windows 10, Chrome |
| **BUG_PROD_002** | Tìm kiếm sản phẩm phân biệt hoa thường không nhất quán | 1. Tìm "dress" (thường)<br>2. Tìm "DRESS" (hoa) | Kết quả trả về giống nhau | Kết quả trả về khác nhau (Logic tìm kiếm chưa tối ưu) | Lớn (Major) | Trung bình | Windows 11, Chrome |
| **BUG_CART_003** | Scroll bị giật khi nhấn "View Cart" từ Popup | 1. Add to cart<br>2. Nhấn "View Cart" trên popup | Chuyển trang mượt mà | Trang bị giật (flicker) một cái rồi mới chuyển | Nhỏ (Minor) | Thấp | MacOS, Safari |
| **BUG_CHK_004** | Nút "Pay and Confirm" có thể click nhiều lần (Double submission) | 1. Điền thông tin thẻ<br>2. Nhấn nút Pay liên tục 5 lần | Chỉ nhận 1 request, disable nút ngay | Gửi đi 5 request, tạo ra 5 đơn hàng trùng nhau (Giả lập) | Nghiêm trọng | Cao | Windows 10, Firefox |
| **BUG_AUTH_005** | Form đăng ký nhận Email: chấp nhận email sai format | 1. Footer -> Subscription<br>2. Nhập "abc" (không có @)<br>3. Submit | Báo lỗi định dạng email | Thông báo "Successfully subscribed!" | Lớn (Major) | Trung bình | All Browsers |
| **BUG_UI_006** | Ảnh quảng cáo (Ads) che mất menu trên Mobile | 1. Mở web trên Mobile (iPhone)<br>2. Vào trang Products | Menu hiển thị rõ ràng | Một banner quảng cáo google che mất 1 phần menu | Lớn (Major) | Cao | iPhone 14, Safari |
| **BUG_PROD_007** | Tiêu đề trang Product Detail bị lỗi font | 1. Vào xem chi tiết 1 SP bất kỳ | Font chữ đồng bộ | Tiêu đề SP bị lỗi font (Times New Roman thay vì Roboto) | Nhỏ (Minor) | Thấp | Windows 10, Edge |
| **BUG_CART_008** | Không cập nhật số lượng khi nhập số thập phân | 1. Vào Cart<br>2. Nhập Quantity = 2.5<br>3. Click ra ngoài | Báo lỗi hoặc làm tròn | Hệ thống tính tiền theo giá x 2.5 (Sai logic nghiệp vụ) | Nghiêm trọng | Trung bình | Windows 10, Chrome |
| **BUG_UI_009** | Nút "Scroll Up" thỉnh thoảng không hoạt động | 1. Cuộn xuống cuối trang<br>2. Nhấn nút mũi tên lên | Cuộn lên đầu trang | Không có phản hồi gì | Nhỏ (Minor) | Thấp | Windows 11, Chrome |
| **BUG_CHK_010** | Tải hóa đơn về bị lỗi định dạng tên file | 1. Payment Success<br>2. Download Invoice | Tên file: invoice.txt | Tên file: inv_@#$%.txt (Lỗi encoding) | Nhỏ (Minor) | Thấp | Windows 10, Chrome |

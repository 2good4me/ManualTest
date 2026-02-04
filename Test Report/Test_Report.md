# Báo cáo kiểm thử (Test Report)

**Dự án**: E-commerce Website  
**Ngày báo cáo**: 04/02/2026  
**Người thực hiện**: Nhóm QA  

## 1. Tổng quan
Đợt kiểm thử này tập trung vào các chức năng cốt lõi: Xác thực, Sản phẩm, Giỏ hàng và Thanh toán. Đã thực thi toàn bộ 45 Ca kiểm thử theo kế hoạch.

## 2. Kết quả thực thi
| Loại | Số lượng | Tỷ lệ (%) |
| :--- | :--- | :--- |
| **Tổng số TC** | 45 | 100% |
| **Đạt (Pass)** | 35 | 77.8% |
| **Trượt (Fail)** | 10 | 22.2% |
| **Chặn (Blocked)** | 0 | 0% |

## 3. Top 5 lỗi nghiêm trọng nhất
1.  **BUG_CART_001** (Nghiêm trọng): Tổng tiền sai khi số lượng lớn.
2.  **BUG_CHK_002** (Nghiêm trọng): Treo khi thanh toán Visa.
3.  **BUG_AUTH_003** (Lớn): Kiểm tra định dạng email yếu.
4.  **BUG_AUTH_006** (Lớn): Chức năng quên mật khẩu hỏng.
5.  **BUG_PROD_004** (Lớn): Bộ lọc giá sai logic.

## 4. Nhận xét chất lượng
*   **Chức năng**: Các luồng chính (Happy Path) của chức năng Mua hàng hoạt động ổn, nhưng gặp lỗi nghiêm trọng ở khâu tính tiền và thanh toán thẻ.
*   **Giao diện**: Còn một số lỗi nhỏ về hiển thị và chính tả, không ảnh hưởng chức năng.
*   **Bảo mật**: Kiểm tra dữ liệu đầu vào còn lỏng lẻo (Email).

## 5. Kết luận & Quyết định
❌ **KHÔNG PHÁT HÀNH (NO-RELEASE)**

**Lý do**: Tồn tại 2 lỗi Nghiêm trọng ảnh hưởng trực tiếp đến doanh thu (tính tiền sai) và trải nghiệm thanh toán. Cần khắc phục gấp và thực hiện Kiểm thử lại (Retest).

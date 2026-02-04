# Báo cáo kiểm thử (Test Report)

**Dự án**: E-commerce Website  
**Ngày báo cáo**: 04/02/2026  
**Người thực hiện**: QA Team  

## 1. Tổng quan (Overview)
Đợt kiểm thử này tập trung vào các chức năng cốt lõi: Authentication, Product, Cart và Checkout. Đã thực thi toàn bộ 45 Test Case theo kế hoạch.

## 2. Kết quả thực thi (Test Execution Results)
| Loại | Số lượng | Tỷ lệ (%) |
| :--- | :--- | :--- |
| **Tổng số TC** | 45 | 100% |
| **Pass** | 35 | 77.8% |
| **Fail** | 10 | 22.2% |
| **Blocked** | 0 | 0% |

## 3. Top 5 lỗi nghiêm trọng nhất
1.  **BUG_CART_001** (Critical): Tổng tiền sai khi số lượng lớn.
2.  **BUG_CHK_002** (Critical): Treo khi thanh toán Visa.
3.  **BUG_AUTH_003** (Major): Validation email yếu.
4.  **BUG_AUTH_006** (Major): Chức năng quên mật khẩu hỏng.
5.  **BUG_PROD_004** (Major): Bộ lọc giá sai logic.

## 4. Nhận xét chất lượng
*   **Chức năng**: Các luồng chính (Happy Path) của chức năng Mua hàng hoạt động ổn, nhưng gặp lỗi nghiêm trọng ở khâu tính tiền và thanh toán thẻ.
*   **Giao diện**: Còn một số lỗi nhỏ về hiển thị và chính tả, không ảnh hưởng chức năng.
*   **Bảo mật**: Validation input còn lỏng lẻo (Email).

## 5. Kết luận & Quyết định (Decision)
❌ **NO-RELEASE** (Không phát hành)

**Lý do**: Tồn tại 2 lỗi Critical ảnh hưởng trực tiếp đến doanh thu (tính tiền sai) và trải nghiệm thanh toán. Cần khắc phục gấp và thực hiện Retest.

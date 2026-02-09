# Chỉ số kiểm thử (Test Metrics)
**Dự án**: Automation Exercise

## 1. Tỷ lệ thực thi Kiểm thử
`100%` (45/45 Test Case đã được thực thi)

## 2. Tỷ lệ Đạt/Trượt (Pass/Fail Rate)
*   **Pass**: 35 Test Case (77.8%)
*   **Fail**: 10 Test Case (22.2%)

## 3. Mật độ lỗi theo Module (Defect Density)
| Module | Số lượng TC | Số lượng Lỗi (Bugs) | Danh sách lỗi | Mật độ |
| :--- | :--- | :--- | :--- | :--- |
| **Xác thực (Auth)** | 15 | 2 | BUG_AUTH_001, BUG_AUTH_005 | 13.3% |
| **Sản phẩm & Giỏ (Prod/Cart)** | 20 | 5 | BUG_PROD_002, BUG_CART_003, BUG_PROD_007, BUG_CART_008, BUG_UI_009 | 25% |
| **Thanh toán (Checkout)** | 10 | 3 | BUG_CHK_004, BUG_UI_006*, BUG_CHK_010 | 30% |
*(Ghi chú: BUG_UI_006 thuộc về giao diện chung nhưng phát hiện khi test luồng mobile)*

## 4. Phân bố mức độ nghiêm trọng (Severity)
| Mức độ | Số lượng | Mã lỗi |
| :--- | :--- | :--- |
| **Nghiêm trọng (Critical)** | 2 | BUG_CHK_004, BUG_CART_008 |
| **Lớn (Major)** | 3 | BUG_PROD_002, BUG_AUTH_005, BUG_UI_006 |
| **Nhỏ (Minor)** | 5 | BUG_AUTH_001, BUG_CART_003, BUG_PROD_007, BUG_UI_009, BUG_CHK_010 |

## 5. Độ bao phủ yêu cầu (Requirement Coverage)
`100%` (16/16 Yêu cầu chức năng đã có Test Case ánh xạ)

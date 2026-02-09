# Chỉ số kiểm thử (Test Metrics)
**Dự án**: Swag Labs

## 1. Tỷ lệ thực thi Kiểm thử
`100%` (35/35 TC)

## 2. Tỷ lệ Đạt/Trượt
*   **Pass**: 28 TC (Test trên Standard User ok)
*   **Fail**: 7 TC (Test trên Problem/Locked User ra bug)

## 3. Mật độ lỗi (Defect Density)
| Module | Số lượng TC | Số lượng Lỗi | Danh sách lỗi |
| :--- | :--- | :--- | :--- |
| **Auth** | 15 | 2 | BUG_AUTH_001, BUG_AUTH_008 |
| **Prod/Cart** | 10 | 4 | BUG_UI_002, BUG_PROD_004, BUG_CART_005, BUG_PROD_009 |
| **Checkout** | 10 | 4 | BUG_CHK_003, BUG_UI_006, BUG_CHK_007, BUG_CHK_010 |

## 4. Phân bố mức độ nghiêm trọng
*   **Critical/Major**: 60% (Các lỗi chức năng của problem_user)
*   **Minor**: 40% (Lỗi giao diện, hiệu năng)

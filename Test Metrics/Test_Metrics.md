# Chỉ số kiểm thử (Test Metrics)

## 1. Tỷ lệ thực thi Kiểm thử
Công thức: `(Số TC đã chạy / Tổng số TC) * 100%`  
Tính toán: `(45 / 45) * 100%`  
**Kết quả: 100%**

## 2. Tỷ lệ Đạt/Trượt
*   **Tỷ lệ Đạt (Pass Rate)**: `(35 / 45) * 100%` = **77.8%**
*   **Tỷ lệ Trượt (Fail Rate)**: `(10 / 45) * 100%` = **22.2%**

## 3. Mật độ lỗi theo Module
| Module | Số lượng Ca kiểm thử | Số lượng Lỗi tìm thấy | Mật độ (Lỗi/TC) |
| :--- | :--- | :--- | :--- |
| Xác thực (Authentication) | 15 | 2 (Bug 003, 006) | 13.3% |
| Sản phẩm & Giỏ hàng | 20 | 5 (Bug 001, 004, 005, 009, UI_007) | 25% |
| Thanh toán (Checkout) | 10 | 3 (Bug 002, 008, 010) | 30% |

## 4. Phân bố mức độ nghiêm trọng
| Mức độ | Số lượng | Tỷ lệ % |
| :--- | :--- | :--- |
| **Nghiêm trọng (Critical)** | 2 | 20% |
| **Lớn (Major)** | 4 | 40% |
| **Nhỏ (Minor)** | 4 | 40% |

## 5. Độ bao phủ yêu cầu
Công thức: `(Số yêu cầu được kiểm tra / Tổng số yêu cầu) * 100%`  
Tính toán: `(16 / 16) * 100%`  
**Kết quả: 100%**

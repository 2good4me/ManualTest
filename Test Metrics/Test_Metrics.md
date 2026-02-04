# Chỉ số kiểm thử (Test Metrics)

## 1. Tỷ lệ thực thi Test (Test Execution Rate)
Công thức: `(Số TC đã chạy / Tổng số TC) * 100%`  
Tính toán: `(45 / 45) * 100%`  
**Kết quả: 100%**

## 2. Tỷ lệ Pass/Fail (Pass/Fail Rate)
*   **Pass Rate**: `(35 / 45) * 100%` = **77.8%**
*   **Fail Rate**: `(10 / 45) * 100%` = **22.2%**

## 3. Mật độ lỗi theo Module (Defect Density per Module)
| Module | Số lượng Test Case | Số lượng Bug tìm thấy | Mật độ (Bug/TC) |
| :--- | :--- | :--- | :--- |
| Authentication | 15 | 2 (Bug 003, 006) | 13.3% |
| Product & Cart | 20 | 5 (Bug 001, 004, 005, 009, UI_007) | 25% |
| Checkout | 10 | 3 (Bug 002, 008, 010) | 30% |

## 4. Phân bố mức độ nghiêm trọng (Severity Distribution)
| Mức độ | Số lượng | Tỷ lệ % |
| :--- | :--- | :--- |
| **Critical** | 2 | 20% |
| **Major** | 4 | 40% |
| **Minor** | 4 | 40% |

## 5. Độ bao phủ yêu cầu (Requirement Coverage)
Công thức: `(Số yêu cầu được test / Tổng số yêu cầu) * 100%`  
Tính toán: `(16 / 16) * 100%`  
**Kết quả: 100%**

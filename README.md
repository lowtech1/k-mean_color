# 🎨 K-Means Color Quantization
---

## 👥 Giới thiệu nhóm
- **Nhóm:** 1  
- **Môn học:** Xử lý ảnh và thị giác máy tính  
- **Đề tài:** 7. Phân cụm màu ảnh bằng thuật toán K-Means  

**Danh sách thành viên:**

| STT | Họ tên                | MSSV         | Ghi chú       |
|-----|-----------------------|--------------|----------------|
| 1   | Phạm Hữu Nhân      | KHDL2211015  |                
| 2   | Huỳnh Vĩnh Cường   | KHDL2211019  |                |

---

## 💡 Giới thiệu đề tài
Dự án ứng dụng **thuật toán K-Means Clustering** để **phân cụm và rút gọn số lượng màu trong ảnh** (color quantization).  
Kết quả giúp tạo ra ảnh với số màu tối giản nhưng vẫn giữ chất lượng hiển thị cao.

**Mục tiêu:**
- Giảm dung lượng ảnh và tăng hiệu quả lưu trữ.  
- Xây dựng mô hình trích xuất bảng màu (palette) đặc trưng cho ảnh.  
- Ứng dụng trong nén dữ liệu ảnh, thị giác máy tính, và thiết kế đồ họa.

---

## 📁 Cấu trúc thư mục

---

## 🧩 Thư viện sử dụng
| Thư viện | Mục đích |
|-----------|-----------|
| **numpy** | Xử lý dữ liệu số và vector hóa pixel |
| **opencv-python (cv2)** | Đọc, ghi và hiển thị ảnh |
| **matplotlib** | Vẽ biểu đồ, hiển thị ảnh gốc và ảnh sau phân cụm |
| **scikit-learn** | Cung cấp thuật toán K-Means |
| **PIL (Pillow)** | Hỗ trợ xử lý ảnh cơ bản |

Cài đặt các thư viện cần thiết:
```
pip install numpy opencv-python matplotlib scikit-learn pillow
```
Hoặc mở qua terminal:
```
jupyter notebook k-mean_color.ipynb

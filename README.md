# 🎨 K-Means Color Quantization
---

## 👥 Giới thiệu nhóm
- **Nhóm:** 1  
- **Môn học:** Hệ cơ sở tri thức  
- **Đề tài:** Phân cụm màu ảnh bằng thuật toán K-Means  

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
jupyter notebook k-mean_color.ipynb
```
k = 8  # số màu cần giữ lại
```
# 1. Import thư viện
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
from PIL import Image
```
# 2. Đọc ảnh và chuyển đổi không gian màu
```
img = cv2.imread("imgs/sample.jpg")
img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
pixels = img.reshape((-1, 3))
```
# 3. Áp dụng K-Means
```
k = 8
kmeans = KMeans(n_clusters=k, random_state=42)
kmeans.fit(pixels)
colors = np.array(kmeans.cluster_centers_, dtype=np.uint8)
labels = kmeans.labels_
```
# 4. Tạo ảnh mới với màu đã được phân cụm
```
quantized = colors[labels].reshape(img.shape)
Image.fromarray(quantized).save("imgs/quantized_k8.jpg")
```
# 5. Hiển thị kết quả
```
plt.figure(figsize=(10,5))
plt.subplot(1,2,1)
plt.title("Ảnh gốc")
plt.imshow(img)
plt.axis("off")

plt.subplot(1,2,2)
plt.title(f"Ảnh sau phân cụm (k={k})")
plt.imshow(quantized)
plt.axis("off")
plt.show()
---

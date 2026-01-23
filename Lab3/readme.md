# Công nghệ sử dụng
- Ngôn ngữ: Python 3
- Thư viện chính
  - OpenCV (cv2) – tính histogram, thresholding (Otsu), đọc và ghi ảnh
  - Matplotlib (plt) – vẽ histogram và hiển thị ảnh so sánh
  - NumPy (np) – thao tác mảng ảnh
- Môi trường: Jupyter Notebook / JupyterLab

# Cách hoạt động chính của code

1. *Tải & chuẩn bị dữ liệu*
   Tải các ảnh mẫu grayscale tiêu chuẩn (Lenna, Baboon, Cameraman, Mammogram,)
   
2. Hàm hỗ trợ trực quan hóa  
   - plot_image(): hiển thị 2 ảnh cạnh nhau 
   - plot_hist(): vẽ histogram so sánh trước, sau xử lý

3. Histogram
   - Sử dụng cv2.calcHist() để tính phân bố cường độ pixel (0–255)  
   - Minh họa bằng toy image 3×3 và các ảnh thực tế

4. Biến đổi cường độ (Intensity Transformations) 
   - Negation (đảo ngược): 255 - pixel
   - Logarithmic: làm sáng vùng tối  
   - Gamma correction: điều chỉnh độ sáng/tối  
   - Contrast stretching – kéo dãn histogram tăng tương phản

5. Ngưỡng hóa & phân đoạn đơn giản (Thresholding)
   - Binary thresholding thủ công  
   - Otsu’s method tự động (cv2.THRESH_OTSU) – tìm ngưỡng tối ưu  
   - Kết quả: ảnh nhị phân giúp tách đối tượng khỏi nền

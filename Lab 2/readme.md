**Những gì em đã học được trong lab 2:**
1. Quản lý đối tượng, bộ nhớ trong Python
- Tham chiếu (Reference) so với Bản copy
2. Thư viện Pillow (PIL)
- Đọc và Hiển thị ảnh: Dùng Image.open() và hiển thị bằng plt.imshow()
- Lật và Xoay ảnh
- Cắt ảnh (Crop): Vẽ lên ảnh Sử dụng mô-đun ImageDraw
3. Thư viện OpenCV (cv2)
Đọc ảnh (BGR): Dùng cv2.imread() để đọc ảnh
Hiển thị đúng màu:
Lật và Xoay ảnh: Sử dụng cv2.flip(image, flipcode) (với flipcode là 0, 1, hoặc -1) hoặc cv2.rotate(image, hằng_số).
Vẽ lên ảnh: Dùng các hàm như cv2.rectangle() và cv2.putText().
 

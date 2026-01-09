QUY TRÌNH XỬ LÝ ẢNH VỚI PIL VÀ OPENCV TRONG PYTHON
1. Quy trình xử lý trong file PIL
(2.1.1_Images_with_python_library_PIL.ipynb)

Quy trình xử lý ảnh trong file này được xây dựng theo hướng lập trình hướng đối tượng, trong đó ảnh được xem như một đối tượng để thao tác trực tiếp.

Khởi tạo và nạp dữ liệu
Quy trình bắt đầu bằng việc import lớp Image từ thư viện PIL và sử dụng Image.open() để nạp ảnh vào chương trình.

Khảo sát thuộc tính ảnh
Sau khi ảnh được nạp, các thuộc tính cơ bản của đối tượng ảnh như width, height, format, và mode được truy xuất trực tiếp để tìm hiểu đặc điểm của ảnh.

Thao tác hình học
Thực hiện các phép biến đổi hình học như:
- Cắt ảnh (crop) bằng cách xác định tọa độ hộp cắt (box).
- Xoay ảnh (rotate) theo một góc xác định.
- Dán ảnh này lên ảnh khác (paste) hoặc ghép nhiều ảnh lại với nhau.

Thao tác màu sắc và pixel
PIL cho phép:
- Tách các kênh màu RGB thành các ảnh riêng biệt.
- Chuyển ảnh sang ảnh xám (Grayscale) hoặc giảm số lượng màu (Quantization).
- Vẽ hình học hoặc chèn văn bản trực tiếp lên ảnh thông qua module ImageDraw.
Kết xuất kết quả
Ảnh sau khi xử lý có thể được lưu ra file mới bằng save() hoặc hiển thị trực tiếp trong Jupyter Notebook.

2. Quy trình xử lý trong file OpenCV
(2.1.2_Images_with_python_library_CV.ipynb)

Quy trình trong file này tiếp cận theo hướng xử lý ảnh như một ma trận số học.

Khởi tạo và nạp dữ liệu
Chương trình bắt đầu bằng việc import thư viện cv2. Ảnh được đọc bằng cv2.imread() và ngay lập tức được lưu dưới dạng một mảng đa chiều (NumPy array).

Chuẩn bị hiển thị ảnh
Do OpenCV sử dụng không gian màu BGR, ảnh cần được chuyển sang RGB bằng cv2.cvtColor() để hiển thị đúng màu khi sử dụng thư viện matplotlib.

Thao tác trên mảng dữ liệu
- Kích thước ảnh được kiểm tra thông qua thuộc tính shape của mảng.
- Cắt ảnh được thực hiện bằng kỹ thuật array slicing theo chỉ số hàng và cột.
- Có thể truy cập và thay đổi trực tiếp từng kênh màu thông qua chỉ số mảng.

Các phép biến đổi ảnh
- Thay đổi kích thước ảnh bằng resize().
- Xoay ảnh thông qua việc tạo ma trận xoay (getRotationMatrix2D) và áp dụng biến đổi affine (warpAffine).

Phân tích ảnh
Biểu đồ Histogram được sử dụng để phân tích sự phân bố cường độ sáng của các kênh màu Red, Green và Blue trong ảnh.

SO SÁNH SỰ KHÁC BIỆT GIỮA PIL VÀ OPENCV
1. Cách đọc ảnh và kiểu dữ liệu
PIL: Sử dụng Image.open(), kết quả là một đối tượng của lớp PIL.
OpenCV: Sử dụng cv2.imread(), kết quả là một mảng NumPy chứa các giá trị số nguyên 8-bit.

2. Không gian màu
PIL: Mặc định sử dụng thứ tự kênh màu RGB.
OpenCV: Mặc định sử dụng thứ tự kênh màu BGR.

3. Cách hiển thị ảnh
PIL: Chỉ cần gọi tên biến ảnh, ảnh sẽ tự động hiển thị trong Notebook.
OpenCV:
cv2.imshow() thường không hoạt động ổn định trong Jupyter Notebook, do đó ảnh được hiển thị bằng matplotlib.pyplot.
Trước khi hiển thị, cần chuyển ảnh từ BGR sang RGB bằng cv2.cvtColor() để tránh sai lệch màu sắc.

4. Cách tiếp cận xử lý
PIL (Hướng đối tượng): Các thao tác xử lý là các phương thức gắn trực tiếp với đối tượng ảnh.
OpenCV (Xử lý ma trận): Các thao tác xử lý thực chất là các phép toán trên mảng số học (NumPy array)

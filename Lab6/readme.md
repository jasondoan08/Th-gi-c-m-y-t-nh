Bài lab này nhằm tìm hiểu các kỹ thuật cơ bản trong Thị giác máy tính (Computer Vision) để phát hiện đặc trưng ảnh (keypoints), phân tích đa tỉ lệ (scale-space) và so khớp đặc trưng giữa các ảnh bằng thư viện OpenCV trong Python.

Mục tiêu là hiểu cách máy tính phân tích nội dung ảnh thông qua các đặc trưng cục bộ và ứng dụng trong nhận dạng, ghép ảnh và tìm kiếm ảnh.

Công nghệ sử dụng:
Python, OpenCV, NumPy, Matplotlib

Nội dung thực hành
1. Harris Corner Detection
Phát hiện các điểm góc (corner) quan trọng trong ảnh.
2. Difference of Gaussians (DoG)
Sử dụng bộ lọc band-pass để làm nổi bật các cấu trúc trong ảnh ở các mức tỉ lệ khác nhau.
3. Automatic Scale Selection
Phân tích ảnh với nhiều mức Gaussian khác nhau để tìm đặc trưng theo tỉ lệ.
4. Scale-Invariant Detection
Sử dụng thuật toán SIFT để phát hiện keypoints không bị ảnh hưởng bởi thay đổi tỉ lệ hoặc xoay.
5. Scale-space Blob Detection
Phát hiện các vùng blob trong ảnh bằng toán tử Laplacian.
6. Bag-of-Words
Nhóm các đặc trưng SIFT bằng K-means để tạo ra các visual words.
7. Image Panorama
Ghép nhiều ảnh có vùng chồng lấp để tạo thành ảnh toàn cảnh.
8. Automatic Image Mosaicing
So khớp keypoints giữa các ảnh để hiển thị các cặp đặc trưng tương ứng.
9. Wide Baseline Stereo
So khớp đặc trưng giữa các ảnh được chụp từ các góc nhìn khác nhau.
10. CBIR (Content-Based Image Retrieval)
So sánh ảnh dựa trên histogram màu để tìm các ảnh có nội dung tương tự.
11. Bag-of-Words với SIFT + Histogram
Biểu diễn ảnh bằng histogram của các visual words được tạo từ đặc trưng SIFT.

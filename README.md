# Depth estimation (Tensorflow)

# Dự đoán độ sâu từ ảnh camera

**Mục tiêu:** Chuyển đổi ảnh chụp thành ảnh độ sâu, hồi quy giá trị khoảng cách của từng pixel. Nhiệm vụ này đặc biệt hữu ích ở những nơi cần cấu trúc cảnh 3D mà không có các phương pháp đo khoảng cách trực tiếp (ví dụ: đo phạm vi, đo âm thanh).

**Đóng góp:**

Với mục đích xây dựng một thư viện bách khoa toàn thư cho thị giác máy tính, nghiên cứu này tập trung vào việc tinh chỉnh các kiến trúc phổ biến hiện nay như **U-net** hoặc kiến trúc **tích chập Autoencoder** để đạt được kết quả tốt với nguồn tài nguyên GPU hạn chế. Các đóng góp chính của nghiên cứu này trong lĩnh vực ước tính độ sâu bao gồm:

1.  **Model CNNs Autoencoder** đơn giản.
2.  **Model CNNs U-net** kết hợp chuẩn **([ResNet](https://arxiv.org/abs/1512.03385))** .
3.  **Model CNNs U-net** kết hợp chuẩn **([DenseNet](https://arxiv.org/abs/1608.06993))** .

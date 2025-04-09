# Depth estimation (Tensorflow)

# Ước lượng độ sâu: Tổng quan và đóng góp

Ước lượng độ sâu là một bài toán quan trọng trong lĩnh vực **thị giác máy tính**. Nó cung cấp thông tin về khoảng cách từ camera đến các điểm hoặc đối tượng trong một cảnh, giúp máy tính hiểu được chiều thứ ba trong không gian 3D. Bài toán này bổ sung thông tin về chiều sâu, cho phép máy tính nắm bắt cấu trúc 3D của vật thể.

**Mục tiêu:** Chuyển đổi ảnh chụp thành ảnh độ sâu, hồi quy giá trị khoảng cách của từng pixel. Nhiệm vụ này đặc biệt hữu ích ở những nơi cần cấu trúc cảnh 3D mà không có các phương pháp đo khoảng cách trực tiếp (ví dụ: đo phạm vi, đo âm thanh).

Cấu trúc các khối:

* **Khối mã hóa (Encoder)**
* **Khối giữa (Middle)**
* **Khối giải mã (Decoder)**

**Đóng góp:**

Với mục đích xây dựng một thư viện bách khoa toàn thư cho thị giác máy tính, nghiên cứu này tập trung vào việc tinh chỉnh các kiến trúc phổ biến hiện nay như **U-net** hoặc kiến trúc **tích chập Autoencoder** để đạt được kết quả tốt với nguồn tài nguyên GPU hạn chế. Các đóng góp chính của nghiên cứu này trong lĩnh vực ước tính độ sâu bao gồm:

1.  **Model CNNs Autoencoder** đơn giản.
2.  **Model CNNs U-net** kết hợp chuẩn **([ResNet](https://arxiv.org/abs/1512.03385))** .
3.  **Model CNNs U-net** kết hợp chuẩn **([DenseNet](https://arxiv.org/abs/1608.06993))** .

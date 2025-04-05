# Depth estimation (Tensorflow)

# Ước lượng độ sâu: Tổng quan và các đóng góp nghiên cứu

Ước lượng độ sâu là một bài toán quan trọng trong lĩnh vực **thị giác máy tính**. Nó cung cấp thông tin về khoảng cách từ camera đến các điểm hoặc đối tượng trong một cảnh, giúp máy tính hiểu được chiều thứ ba trong không gian 3D. Bài toán này bổ sung thông tin về chiều sâu, cho phép máy tính nắm bắt cấu trúc 3D của vật thể.

**Mục tiêu:** Chuyển đổi ảnh chụp thành ảnh độ sâu, hồi quy giá trị khoảng cách của từng pixel. Nhiệm vụ này đặc biệt hữu ích ở những nơi cần cấu trúc cảnh 3D mà không có các phương pháp đo khoảng cách trực tiếp (ví dụ: đo phạm vi, đo âm thanh).

**Bối cảnh và các nghiên cứu gần đây:**

Từ khoảng năm 2014 đến nay, bài toán ước lượng độ sâu đã chứng kiến sự nghiên cứu và phát triển mạnh mẽ với nhiều kiến trúc mô hình khác nhau, tiêu biểu là các kiến trúc gần đây như **ZoeDepth**, **Marigold**, **PrimeDepth**, v.v.

Điểm chung của các nghiên cứu này là kiến trúc tổng quát dạng **Autoencoder**, bao gồm các khối:

* **Khối mã hóa (Encoder)**
* **Khối giữa (Middle)**
* **Khối giải mã (Decoder)**

Điểm khác biệt giữa các nghiên cứu nằm ở nhiều khía cạnh sâu sắc, bao gồm:

* Cấu hình của khối Middle
* Tỷ lệ kích thước giữa khối Encoder và Decoder
* Kết nối tắt (skip connections) giữa Encoder và Decoder

**Đóng góp nghiên cứu:**

Với mục đích xây dựng một thư viện bách khoa toàn thư cho thị giác máy tính, nghiên cứu này tập trung vào việc tinh chỉnh các kiến trúc phổ biến hiện nay như **U-net** hoặc kiến trúc **tích chập Autoencoder** để đạt được kết quả tốt với nguồn tài nguyên GPU hạn chế. Các đóng góp chính của nghiên cứu này trong lĩnh vực ước tính độ sâu bao gồm:

1.  **Mô hình kiến trúc mạng tích chập Autoencoder** kết hợp chuẩn mô hình **DenseNet** được tinh chỉnh.
2.  **Mô hình kiến trúc mạng tích chập U-net** kết hợp chuẩn **([Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385))** được tinh chỉnh.
3.  **Mô hình kiến trúc mạng tích chập U-net** kết hợp chuẩn **DenseNet (Densely Connected Convolutional Networks)** được tinh chỉnh.

# Depth Estimation

*`Ước lượng độ sâu`* kỹ thuật này tính toán khoảng cách từ cảm biến (thường là camera) đến từng điểm hoặc đối tượng hiện hữu trong một khung cảnh quan sát được. Thông qua việc hồi quy giá trị độ sâu cho mỗi điểm ảnh.

*`Mục tiêu chính`* Thay thế các thiết bị đo độ sâu chuyên dụng (LiDAR, PrimeSense Carmine sensor, ..) bằng các phương pháp huấn luyện mô hình học sâu dựa trên CNNs  
*`Ứng dụng`* 
<ul>
  <lu>
    1. Xe tự hành (sử dụng dữ liệu độ sâu từ các cảm biến để xây dựng mô hình 3D chi tiết của môi trường xung quanh xe, kết hợp với các biện pháp xác định vị trí các đối tượng trong ảnh RGB từ đó xác định khoảng cách khi có vật đến gần để xe vận hành tự động). ![image](https://github.com/user-attachments/assets/be50dbaa-d2f2-4e3a-bdb8-79dd2eabc77b)
  </lu>
  
  <lu>
    2. ![image](https://github.com/user-attachments/assets/e72ca09a-88f2-4fb9-b9cf-fa1b01cd5619)

  </lu>
</ul>


1.  **Model CNNs Autoencoder** đơn giản.
2.  **Model CNNs U-net** kết hợp chuẩn **([ResNet](https://arxiv.org/abs/1512.03385))** .
3.  **Model CNNs U-net** kết hợp chuẩn **([DenseNet](https://arxiv.org/abs/1608.06993))** .

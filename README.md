# Depth estimation (Tensorflow)

# Dự đoán độ sâu từ ảnh camera

**Mục tiêu chính:** Thay thế các thiết bị đo độ sâu chuyên dụng (LiDAR, PrimeSense Carmine sensor, ..) bằng các phương pháp huấn luyện mô hình học sâu dựa trên CNNs  
**Ứng dụng:** 
<ul>
  <lu>
    1. Xe tự hành (sử dụng dữ liệu độ sâu từ các cảm biến để xây dựng mô hình 3D chi tiết của môi trường xung quanh xe, kết hợp với các biện pháp xác định vị trí các đối tượng trong ảnh RGB từ đó xác định khoảng           cách khi có vật đến gần để xe vận hành tự động). ![image](https://github.com/user-attachments/assets/be50dbaa-d2f2-4e3a-bdb8-79dd2eabc77b)

  </lu>
  <lu></lu>
</ul>


1.  **Model CNNs Autoencoder** đơn giản.
2.  **Model CNNs U-net** kết hợp chuẩn **([ResNet](https://arxiv.org/abs/1512.03385))** .
3.  **Model CNNs U-net** kết hợp chuẩn **([DenseNet](https://arxiv.org/abs/1608.06993))** .

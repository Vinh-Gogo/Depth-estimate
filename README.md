<h1>Depth Estimation</h1>

## Ước lượng độ sâu
Kỹ thuật này tính toán khoảng cách từ cảm biến (thường là camera) đến từng điểm hoặc đối tượng hiện hữu trong một khung cảnh quan sát được. Thông qua việc hồi quy giá trị độ sâu cho mỗi điểm ảnh.

## Mục tiêu chính
Thay thế các thiết bị đo độ sâu chuyên dụng (LiDAR, PrimeSense Carmine sensor, ..) bằng các phương pháp huấn luyện mô hình học sâu dựa trên CNNs  

## Ứng dụng

1. Xe tự hành (sử dụng dữ liệu độ sâu từ các cảm biến để xây dựng mô hình 3D chi tiết của môi trường xung quanh xe, kết hợp với các biện pháp xác định vị trí các đối tượng trong ảnh RGB từ đó xác định khoảng cách khi có vật đến gần để xe vận hành tự động)
   
<img src="https://github.com/user-attachments/assets/a5edf6a8-3b16-470b-a7ff-d5cf4efd2a7d" width="500"/>

2. Tái tạo 3D
   
<img src="https://github.com/user-attachments/assets/721f5793-581f-4f14-89d7-d85909125f89" width="500"/>

<h2>Phương pháp</h2>
  
1.  **Convolutional Autoencoder (CAE) backbone [ResNet](https://arxiv.org/abs/1512.03385)**
  
<img src="https://github.com/user-attachments/assets/9052fb4b-f523-4288-888f-6a4effb3ab34" width="300"/>
<img src="https://github.com/user-attachments/assets/7c9073ea-37e2-465e-b46e-e383f936efab" width="440"/>

2.  **U-net backbone [ResNet](https://arxiv.org/abs/1512.03385)**

<img src="https://github.com/user-attachments/assets/06824744-781b-4048-8b7e-87095958df39" width="310"/>
<img src="https://github.com/user-attachments/assets/1b1ce28e-d5a8-4b09-b38d-1be68497bb12" width="430"/>

3.  **U-net backbone kết hợp [ResNet](https://arxiv.org/abs/1512.03385) & [DenseNet](https://arxiv.org/abs/1608.06993)**

<img src="https://github.com/user-attachments/assets/a1e1695e-19e9-4ab0-9e1d-48e30c93b78c" width="330"/>
<img src="https://github.com/user-attachments/assets/d5df4059-7967-4873-a993-6ac6fe999f1a" width="400"/>

4. **Unet SE resnet-dense (light - 3M)**

![alt text](image.png)

5. **Unet SE resnet-dense (light - 7M)**

![alt text](image-2.png)

6. **Unet SE resnet-dense (medium - 13M)**

![alt text](image-1.png)
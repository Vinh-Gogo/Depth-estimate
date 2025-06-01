<h1>Depth Estimation</h1>

## Ước lượng độ sâu
Kỹ thuật này tính toán khoảng cách từ cảm biến (thường là camera) đến từng điểm hoặc đối tượng hiện hữu trong một khung cảnh quan sát được. Thông qua việc hồi quy giá trị độ sâu cho mỗi điểm ảnh.

## Mục tiêu chính
Thay thế các thiết bị đo độ sâu chuyên dụng (LiDAR, PrimeSense Carmine sensor, ..) bằng các phương pháp huấn luyện mô hình học sâu dựa trên CNNs  

## Ứng dụng

1. Xe tự hành (sử dụng dữ liệu độ sâu từ các cảm biến để xây dựng mô hình 3D chi tiết của môi trường xung quanh xe, kết hợp với các biện pháp xác định vị trí các đối tượng trong ảnh RGB từ đó xác định khoảng cách khi có vật đến gần để xe vận hành tự động))
   
<img src="https://github.com/user-attachments/assets/a5edf6a8-3b16-470b-a7ff-d5cf4efd2a7d" width="500"/>

3. Tái tạo 3D
   
<img src="https://github.com/user-attachments/assets/721f5793-581f-4f14-89d7-d85909125f89" width="500"/>

<h2>Phương pháp</h2>
  
1.  **Convolutional Autoencoder (CAE) backbone [ResNet](https://arxiv.org/abs/1512.03385)**
  
<img src="https://github.com/user-attachments/assets/9052fb4b-f523-4288-888f-6a4effb3ab34" width="300"/>
<img src="https://github.com/user-attachments/assets/7c9073ea-37e2-465e-b46e-e383f936efab" width="440"/>

3.  **U-net backbone [ResNet](https://arxiv.org/abs/1512.03385)**

<img src="https://github.com/user-attachments/assets/06824744-781b-4048-8b7e-87095958df39" width="300"/>
<img src="https://github.com/user-attachments/assets/1b1ce28e-d5a8-4b09-b38d-1be68497bb12" width="420"/>

4.  **U-net backbone kết hợp [ResNet](https://arxiv.org/abs/1512.03385) & [DenseNet](https://arxiv.org/abs/1608.06993)**

<img src="https://github.com/user-attachments/assets/a1e1695e-19e9-4ab0-9e1d-48e30c93b78c" width="330"/>
<img src="https://github.com/user-attachments/assets/d5df4059-7967-4873-a993-6ac6fe999f1a" width="400"/>

## Kết quả dự đoán

1 & 2. CAE backbone [ResNet](https://arxiv.org/abs/1512.03385) & U-net backbone [ResNet](https://arxiv.org/abs/1512.03385)
   
![image](https://github.com/user-attachments/assets/6dbfd698-ce0e-419a-b76e-e73ef4223d01)

![image](https://github.com/user-attachments/assets/b8d430e7-d5da-45e2-9605-f6f20c4f6acc)

3. U-net backbone kết hợp [ResNet](https://arxiv.org/abs/1512.03385) & [DenseNet](https://arxiv.org/abs/1608.06993)
   
![image](https://github.com/user-attachments/assets/4971a974-1753-4ae4-a15c-f529e2668f5b)

![image](https://github.com/user-attachments/assets/43b041cf-fb73-4804-aeed-1540b9b2c4d1)


## So sánh

![image](https://github.com/user-attachments/assets/d102748f-7e52-48bc-83a7-ce35209c122f)

## Số lượng ảnh có độ lớn tin cậy với ngưỡng khác nhau 10%

![image](https://github.com/user-attachments/assets/4753e80e-5fe4-475f-9f7e-10c40fe383fa)

![image](https://github.com/user-attachments/assets/18135011-16ec-4d6c-8f5b-4ac6f333d8f0)

![image](https://github.com/user-attachments/assets/9a45071e-98e1-4fe9-b5e3-5592f1065944)

<h1>Depth Estimation</h1>

## Ước tính khoảng cách từ camera đến các vật thể trong ảnh
## Estimate the distance from the camera to objects in the image

<h2>Kiến trúc mô hình - Models architecture</h2>
  
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



5. **Unet SE resnet-dense (light - 7M)**



6. **Unet SE resnet-dense (medium - 13M)**

- backbone:
    + se block
    + conv_se_block
    + densenet-resnet block
    + attention block

![alt text](image-1.png)

## Evalute model 6

![alt text](image-3.png)
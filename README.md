# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
</br>
Import the required libraries.
</br> 

### Step2
</br>

Convert the image from BGR to RGB.
</br> 

### Step3
</br>
Apply the required filters for the image separately.
</br> 

### Step4
</br>
Plot the original and filtered image by using matplotlib.pyplot.
</br> 

### Step5
</br>
End the program.
</br> 

## Program:
### Developed By : DEEPIKA R
### Register Number: 212223230038
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("rose.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```
ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()

```
iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv)Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.title("Median Blur")
plt.axis('off')
plt.show()

```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()

```
ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()

```

## OUTPUT:
### 1. Smoothing Filters


i) Using Averaging Filter
<img width="807" height="255" alt="image" src="https://github.com/user-attachments/assets/f9a6744d-3aa8-406b-a346-9982ad289b41" />

ii)Using Weighted Averaging Filter
<img width="578" height="375" alt="image" src="https://github.com/user-attachments/assets/fad0e445-a29a-4bfe-8d56-0704371e4753" />

iii)Using Gaussian Filter
<img width="570" height="365" alt="image" src="https://github.com/user-attachments/assets/92e47ec2-6d91-478a-ac8f-cfda3caa7aed" />

iv) Using Median Filter
<img width="569" height="336" alt="image" src="https://github.com/user-attachments/assets/019ed0da-49d4-462b-904b-6b4c2cca10a9" />

### 2. Sharpening Filters


i) Using Laplacian Kernal
<img width="569" height="368" alt="image" src="https://github.com/user-attachments/assets/e5838560-4270-4bce-a051-f864a38eb9b3" />

ii) Using Laplacian Operator
<img width="569" height="361" alt="image" src="https://github.com/user-attachments/assets/43f21bff-e6a0-478e-8974-7bd2ad41bb2e" />

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.

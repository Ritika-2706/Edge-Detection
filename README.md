# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>
Import the required packages for further process.
### Step2:
<br>
Read the image and convert the bgr image to gray scale image.

### Step3:
<br>
Use any filters for smoothing the image to reduse the noise.

### Step4:
<br>

Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.
### Step5:
<br>
Display the filtered image using plot and imshow.
 
## Program:
```
# Import the packages

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("stark.jpg")

# Load the image, Convert to grayscale and remove noise

gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)

# SOBEL EDGE DETECTOR

# SOBEL X

sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img)
plt.title('Image')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap='Greys')
plt.title("Sobel X")
plt.xticks([])
plt.yticks([])
plt.show()

# SOBEL Y
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img)
plt.title('Image')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap='Greys')
plt.title("Sobel-Y")
plt.xticks([])
plt.yticks([])
plt.show()

# SOBEL XY
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img)
plt.title('Image')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap='Greys')
plt.title("Sobel XY")
plt.xticks([])
plt.yticks([])
plt.show()

# LAPLACIAN EDGE DETECTOR
laplacian = cv2.Laplacian(image,cv2.CV_64F)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img)
plt.title('Image')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap='gray')
plt.title("Laplacian")
plt.xticks([])
plt.yticks([])
plt.show()

# CANNY EDGE DETECTOR
canny_edges = cv2.Canny(image, 120, 150)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img)
plt.title('Image')
plt.subplot(1,2,2)
plt.imshow(canny_edges,cmap='gray')
plt.title("Canny Edges")
plt.xticks([])
plt.yticks([])
plt.show()
```

## Output:
### SOBEL EDGE DETECTOR

![Output](![image1](https://user-images.githubusercontent.com/93427238/169309129-5d3225e9-f507-4c6a-b290-9c4e17addde4.png)
![Output](![image2](https://user-images.githubusercontent.com/93427238/169309187-7fbe85b6-45c4-4a2b-a52f-d1c110fcc23c.png)
![Output](![image3](https://user-images.githubusercontent.com/93427238/169309239-84f1713b-871a-4f16-a7c4-0c81d379e847.png)



### LAPLACIAN EDGE DETECTOR

![Output](![image4](https://user-images.githubusercontent.com/93427238/169309545-6f137704-9499-4ff6-9b7e-99d36f39d29b.png)


### CANNY EDGE DETECTOR
![Output](![image5](https://user-images.githubusercontent.com/93427238/169309741-e67ab447-f6e1-473a-a48f-4aa39022a987.png)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step1:

Import the required packages for further process.

### step2:

Read the image and convert the bgr image to gray scale image.


### Step3:

Use any filters for smoothing the image to reduse the noise.

### Step4:

Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step5:

Display the filtered image using plot and imshow.

 
## Program:

### SOBRL X:

```

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("Imagee.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel-X")
plt.xticks([])
plt.yticks([])
plt.show()

```

### SOBEL Y:
```

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("image.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='Purples')
plt.title('Purples')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap='Purples')
plt.title("Sobel-Y")
plt.xticks([])
plt.yticks([])
plt.show()

```

## SOBEL XY:

```

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("imagee.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='Oranges')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap='Oranges')
plt.title("Sobel-XY")
plt.xticks([])
plt.yticks([])
plt.show()

```

 ## LAPLACIAN EDGE DETECTOR

```

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("image1.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
laplacian = cv2.Laplacian(img,cv2.CV_64F)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='Blues')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap='Blues')
plt.title("Laplacian")
plt.xticks([])
plt.yticks([])
plt.show()

```


### CANNY EDGE DETECTOR

```

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("image.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
canny_edges = cv2.Canny(image, 120, 150)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(canny_edges,cmap='gray')
plt.title("Canny_edges")
plt.xticks([])
plt.yticks([])
plt.show()

```

# Output:

## SOBEL EDGE DETECTOR

### SOBEL X:

![OUTPUT](./output1.png)

### SOBEL Y:

![output2](https://user-images.githubusercontent.com/93427240/168266673-c39197fe-91bc-4f05-9552-f3944bbd3291.png)


### SOBEL XY:

![output3](https://user-images.githubusercontent.com/93427240/168266699-03ec2f7a-f60c-4f35-84bf-5ae112ba3a33.png)

## LAPLACIAN EDGE DETECTOR

![output4](https://user-images.githubusercontent.com/93427240/168266764-76cd8ffe-e403-4bf8-b9ba-db04fe71114c.png)


## CANNY EDGE DETECTOR

![output5](https://user-images.githubusercontent.com/93427240/168266795-8c9db5d8-90d2-42aa-917c-8ef147357cdb.png)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

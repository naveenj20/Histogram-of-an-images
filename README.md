# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: Naveen Jaisanker
# Register Number: 212224110039

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("grayscale-image.jpg")
color_image = cv2.imread("flower.jpg")
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Color Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

import numpy as np
import cv2
Gray_image = cv2.imread("grayscale-image.jpg")
Color_image = cv2.imread("flower.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)

import cv2
gray_image = cv2.imread("grayscale-image.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:

### Input Grayscale Image and Color Image

![Screenshot 2025-04-23 113535](https://github.com/user-attachments/assets/f1a51e82-eebd-4670-a33d-48a7e4975da6)

![Screenshot 2025-04-23 113547](https://github.com/user-attachments/assets/02add1f9-7636-4bc2-a4f5-b06f1a5d9783)


### Histogram of Grayscale Image and any channel of Color Image

![Screenshot 2025-04-23 113633](https://github.com/user-attachments/assets/e3781197-38d9-41f4-84bf-ff503114fab7)

### Histogram Equalization of Grayscale Image.

![Screenshot 2025-04-23 113714](https://github.com/user-attachments/assets/8974f0cd-4b91-4780-b4f3-3b0e57b00d20)


## Result: 

Thus, the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also, histogram equalization is done for the gray scale image using OpenCV.

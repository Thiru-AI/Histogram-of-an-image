# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.
<br>

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.
<br>

### Step3:
Display the histograms with their respective images.
<br>

### Step4:
Equalize the grayscale image.
<br>

### Step5:
Display the grayscale image.
<br>

## Program:
```python
# Developed By: G.Thirugnanamoorthi
# Register Number: 212221230117

# Write your code to find the histogram of gray scale image and color image channels.

import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('1.jfif')
plt.imshow(Gray_image)
plt.show()
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()




# Display the histogram of gray scale image and any one channel histogram from color image

import cv2
import matplotlib.pyplot as plt
Color_image=cv2.imread('2.jfif')
plt.imshow(Color_image)
plt.show()
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()




# Write the code to perform histogram equalization of the image. 

import cv2
gray_image = cv2.imread("2.jfif",0)
cv2.imshow('grey scale image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows 






```
## Output:
### Input Grayscale Image and Color Image
![1](https://user-images.githubusercontent.com/94980741/165251320-3d787c30-44ad-4e2c-a084-2ef03c35818e.png)

<br>

### Histogram of Grayscale Image and any channel of Color Image
![2](https://user-images.githubusercontent.com/94980741/165251469-7efb5599-e9c2-4026-aacb-97f15b2b4029.png)

<br>

### Histogram Equalization of Grayscale Image
![grey scale image](https://user-images.githubusercontent.com/94980741/165251636-cc408512-3224-4f03-bfaf-154a4ea5a786.png)

![Equalized Image](https://user-images.githubusercontent.com/94980741/165251674-e0e70492-24d9-408f-94c5-7143ebeb40e6.png)


<br>


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.

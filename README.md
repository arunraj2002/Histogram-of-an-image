# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread().
<br>

### Step2:
Print the image using imshow().
<br>

### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image
<br>

### Step4:
cv2.equalize() is used to transform the gray image to equalized form.
<br>

### Step5:
The Histogram of gray scale image and color image is shown.
<br>

## Program:
```python
# Developed By: R ARUNRAJ
# Register Number: 212220230004

# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
#gray scale and color image
gray_image = cv2.imread("gray.jpg")
color_image = cv2.imread("tata.jpg")
#resizing and printing the image
gray_image= cv2.resize(gray_image, (300,170))
cv2.imshow('GRAY IMAGE',gray_image)
color_image= cv2.resize(color_image, (300,170))
cv2.imshow('COLOR IMAGE',color_image)
cv2.waitKey(0)

# Display the histogram of gray scale image and any one channel histogram from color image.
gray_hist=cv2.calcHist([gray],[0],None,[256],[0,255])
color_hist=cv2.calcHist([color],[2],None,[256],[0,255])
plt.figure()
plt.title("GRAY IMAGE")
plt.xlabel("GRAYSCALE VALUE")
plt.ylabel("PIXEL COUNT")
plt.stem(gray_hist)
plt.show()
plt.figure()
plt.title("COLOR IMAGE")
plt.xlabel("COLORSCALE VALUE")
plt.ylabel("PIXEL COUNT")
plt.stem(color_hist)
plt.show()

# Write the code to perform histogram equalization of the image. 
import cv2
Gray_image=cv2.imread('gray.jpg',0)
equalize=cv2.equalizeHist(Gray_image)
#resizing image
Gray_image= cv2.resize(Gray_image, (270,190))
equalize= cv2.resize(equalize, (270,190))
#output
cv2.imshow('GRAY IMAGE',Gray_image)
cv2.imshow('EQUALIZED IMAGE',equalize)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
![Screenshot (419)](https://user-images.githubusercontent.com/75235747/165152059-4d28bbb6-ebd3-474a-91d4-64cdd0097dc8.png)
<br>

### Histogram of Grayscale Image and any channel of Color Image
![histo](https://user-images.githubusercontent.com/75235747/165152152-6069bdfb-1b7d-453e-a014-b29dc6056f66.JPG)
<br>
![histogram](https://user-images.githubusercontent.com/75235747/165152172-c4211e6d-57f6-492b-8931-782ebd695db1.png)
<br>

### Histogram Equalization of Grayscale Image
![Screenshot (429)](https://user-images.githubusercontent.com/75235747/165152256-144540c9-6279-4b3d-9c47-ba177f3186a1.png)

<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.

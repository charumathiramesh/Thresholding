# Thresholding of Images
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:


### Step2:


### Step3:


### Step4:


### Step5:


## Program

```python
NAME : CHARUMATHI R
REF NO : 212222240021
# Load the necessary packages
import cv2
import matplotlib.pyplot as plt
import numpy as np




# Read the Image and convert to grayscale
image=cv2.imread("image.jpeg")
image1=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)



# Use Global thresholding to segment the image
ret, thresh1 = cv2.threshold(image1,100,200,cv2.THRESH_BINARY)
ret, thresh2 = cv2.threshold(image1,100,200,cv2.THRESH_BINARY_INV)
ret, thresh3 = cv2.threshold(image1,100,200,cv2.THRESH_TRUNC)
ret, thresh4 = cv2.threshold(image1,100,200,cv2.THRESH_TOZERO)
ret, thresh5 = cv2.threshold(image1,100,200,cv2.THRESH_TOZERO_INV)



# Use Adaptive thresholding to segment the image

th1=cv2.adaptiveThreshold(image1,255,cv2.ADAPTIVE_THRESH_MEAN_C,cv2.THRESH_BINARY,11,2)
th2=cv2.adaptiveThreshold(image1,255,cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY,11,2)


# Use Otsu's method to segment the image 
ret2,th3 = cv2.threshold(image1,0,255,cv2.THRESH_BINARY+cv2.THRESH_OTSU)



# Display the results
titles=["Gray Image","THRESH_BINARY","THRESH_BINARY_INV","THRESH_TRUNC"
       ,"THRESH_TOZERO","THRESH_TOZERO_INV","ADAPTIVE_THRESH_MEAN_C","ADAPTIVE_THRESH_GAUSSIAN_C","OTSU"]
images=[image1,thresh1,thresh2,thresh3,thresh4,thresh5,th1,th2,th3]
for i in range(0,9):
    plt.figure(figsize=(10,10))
    plt.subplot(1,2,1)
    plt.title("Original Image")
    plt.imshow(image)
    plt.axis("off")
    plt.subplot(1,2,2)
    plt.title(titles[i])
    plt.imshow(cv2.cvtColor(images[i],cv2.COLOR_BGR2RGB))
    plt.axis("off")
    plt.show()




```
## Output

### Original Image
![download](https://github.com/charumathiramesh/Thresholding/assets/120204455/59487456-5ef8-4409-9c28-065f3469acf5)



### Global Thresholding
![download](https://github.com/charumathiramesh/Thresholding/assets/120204455/01e8e584-1313-4a52-8782-67023eb6d818)
![download](https://github.com/charumathiramesh/Thresholding/assets/120204455/a52de513-b939-4dda-a072-b013148b7d10)

![download](https://github.com/charumathiramesh/Thresholding/assets/120204455/d7fdf0ce-e242-47b5-8a6c-fdcace6dbc98)

![download](https://github.com/charumathiramesh/Thresholding/assets/120204455/64ef60d5-6a39-45a3-9979-bede2394931e)
![download](https://github.com/charumathiramesh/Thresholding/assets/120204455/ecf6a1d1-e798-41c8-b60c-30e4450f30e8)




### Adaptive Thresholding
![download](https://github.com/charumathiramesh/Thresholding/assets/120204455/9125b773-2656-42f4-87a0-2e51d5221883)
![download](https://github.com/charumathiramesh/Thresholding/assets/120204455/a74aa19f-b8c5-478a-abaf-25f875418634)




### Optimum Global Thesholding using Otsu's Method

![download](https://github.com/charumathiramesh/Thresholding/assets/120204455/70908eae-bf70-4ba5-bdca-5f94f2ad8393)

## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.


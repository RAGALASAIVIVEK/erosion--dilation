# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image
 
## Program:
## Developed by: M MANI SRI LATHA
## Register number: 212223110025
## PROGRAM
```
#exp-9-Erosion & Dilation
import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'MANI SRI' ,(5,70),font,4,(255),2,cv2.LINE_AA)


# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

# Display the results
plt.figure(figsize=(12, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')
```
## Output:

### Display the input Image
![Screenshot 2025-05-04 143757](https://github.com/user-attachments/assets/483e1e73-9651-4c4c-931f-68bce36a6ba5)

### Display the Eroded Image
![Screenshot 2025-05-04 143807](https://github.com/user-attachments/assets/6aa743a4-530c-483e-a36e-cd28f5e61100)


### Display the Dilated Image
![Screenshot 2025-05-04 143836](https://github.com/user-attachments/assets/cfcc4ed4-a12e-4536-912c-f0b57c2fd662)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.

# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation
 
## Program:
```
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt
# Load the Image
img1=np.zeros((100,600),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
# Create the Text using cv2.putText
cv2.putText(img1,' GRAND THEFT AUTO ',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()
# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
# Use Opening operation
image1=cv2.morphologyEx(im,cv2.MORPH_OPEN,kernel1)
plt.imshow(image1,cmap='gray')
plt.title('OPENING'), plt.xticks([]), plt.yticks([])
plt.show()
# Use Closing Operation
image1=cv2.morphologyEx(im,cv2.MORPH_CLOSE,kernel1)
plt.imshow(image1,cmap='gray')
plt.title('CLOSING'), plt.xticks([]), plt.yticks([])
plt.show()
```
## Output:

### Display the input Image

![image](https://github.com/Bhuvaneshwari-2003/OPENING--CLOSING/assets/94828604/66aa75f6-7a0b-4f86-b5dd-100deab74a96)

### Display the result of Opening
![image](https://github.com/Bhuvaneshwari-2003/OPENING--CLOSING/assets/94828604/72f6861f-1451-4ccb-9b74-2cc79b64b9b7)

### Display the result of Closing
![image](https://github.com/Bhuvaneshwari-2003/OPENING--CLOSING/assets/94828604/244ed8b6-2dea-4dcd-b733-84167e9a7bb3)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.

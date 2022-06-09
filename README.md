# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step 1:
Import the necessary packages.
<br>

### Step 2:
Create the Text using cv2.putText.
<br>

### Step 3:
Create the structuring element
<br>

### Step 4:
Use Opening operation
<br>

### Step 5:
Use Closing Operation
<br>

 
## Program:

``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt
# Load the Image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
# Create the Text using cv2.putText
cv2.putText(img1,' WAKANDA FOREVER ',(5,70),font,2,(255),5,cv2.LINE_AA)
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
![OUTPUT](11.jpg)
<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
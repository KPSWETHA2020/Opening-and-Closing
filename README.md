# OPENING AND CLOSING

## AIM:
To implement Opening and Closing using Python and OpenCV.

## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Use Opening operation.
### Step 5:
Use Closing Operation.

## PROGRAM:
```
/*
Developed by   : Swetha.k.p
Register Number: 212220230053
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'Kavya',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation
image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()

# Use Closing Operation
image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()

```
## OUTPUT:

### Display the input Image
![image](https://user-images.githubusercontent.com/75235209/171095048-5e6d7b84-8ce3-4a18-8ee6-40aa0079e3d7.png)

### Display the result of Opening
![image](https://user-images.githubusercontent.com/75235209/171095118-7627d9bc-7aa0-4ebd-b124-3de9da9050f6.png)

### Display the result of Closing
![image](https://user-images.githubusercontent.com/75235209/171095172-9610d918-26bb-4f24-9719-11e7a9e6ac21.png)

## RESULT:
Thus the Opening and Closing operation is used in the image using python and OpenCV.

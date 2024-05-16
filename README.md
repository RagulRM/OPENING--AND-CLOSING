# EXP-10 OPENING AND CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages
### Step2:
Give the input text using cv2.putText()
### Step3:
Perform opening operation and closing operations.
### Step4:
Display the result.

## Program:

### Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```python
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Euphoria',(5,70), font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1)
plt.axis("off")
```
### Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
### Use Opening operation
```python
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```
### Use Closing Operation
```python
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:

### Display the input Image
<br>

![image](https://github.com/RagulRM/OPENING--AND-CLOSING/assets/121609342/048724f7-ea98-4f91-9542-d391ee916adb)

<br>

### Display the result of Opening
<br>

![image](https://github.com/RagulRM/OPENING--AND-CLOSING/assets/121609342/87a5bc25-473a-4848-adac-b3f93a49a77b)

<br>

### Display the result of Closing
<br>

![image](https://github.com/RagulRM/OPENING--AND-CLOSING/assets/121609342/ef59865b-ab82-4105-af59-db57da1d3827)

<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.

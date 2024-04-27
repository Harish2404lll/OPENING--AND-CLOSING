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
Create the structuring element.

### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.
 
## Program:
```
DEVELOPED BY: HARISH G
REGISTER NO: 212222243001
```
### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'Buna', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```
### Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
### Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")
```
### Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")
```
## Output:

### Display the input Image
![Screenshot 2024-04-27 135558](https://github.com/Harish2404lll/OPENING--AND-CLOSING/assets/141472096/2c6ced99-4f03-4cba-b454-f4c6515d787f)


### Display the result of Opening
![Screenshot 2024-04-27 135604](https://github.com/Harish2404lll/OPENING--AND-CLOSING/assets/141472096/b05c41b5-364e-4af4-bab2-37570a14e332)



### Display the result of Closing
![Screenshot 2024-04-27 135610](https://github.com/Harish2404lll/OPENING--AND-CLOSING/assets/141472096/9e3bff1b-d334-410c-b79e-216c1971a39a)



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.

# EX-10 OPENING--AND-CLOSING
# Developed By: Markandeyan Gokul
# Reg.No: 212224240086

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

### Step1:
Import the necessary packages

### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation


## Program:

## Import the necessary packages
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

## Create the Text using cv2.putText
```python
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'Gokul', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```

## Create the structuring element
```python
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```

## Use Opening operation
```python
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")
```
## Use Closing Operation
```python
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")
```
## Output:
### Display the input Image
<img width="811" height="188" alt="image" src="https://github.com/user-attachments/assets/be86976e-acd2-4050-8ea2-e0fc5f709968" />

### Display the result of Opening
<img width="813" height="191" alt="image" src="https://github.com/user-attachments/assets/e35d6f81-244f-427d-a1c9-4a8565b7e20b" />

### Display the result of Closing
<img width="793" height="200" alt="image" src="https://github.com/user-attachments/assets/f9fe98ce-866a-441a-9641-a0748580a548" />

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.

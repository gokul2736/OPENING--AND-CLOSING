# EX-10 OPENING--AND-CLOSING
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
# DEVELOPED BY: Markandeyan Gokul
# REGISTER NO: 212224240086

# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'HARIKA', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```
# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
# Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")
```
# Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")
```
## Output:

### Display the input Image
<img width="665" height="175" alt="Screenshot 2025-10-10 183348" src="https://github.com/user-attachments/assets/f965c23a-4eaf-4c62-9eed-143f38f937f4" />

### Display the result of Opening
<img width="662" height="171" alt="Screenshot 2025-10-10 183359" src="https://github.com/user-attachments/assets/d424e687-eb0d-47b7-88c8-d02f5b1c9673" />

### Display the result of Closing
<img width="655" height="160" alt="Screenshot 2025-10-10 183408" src="https://github.com/user-attachments/assets/96b65fab-c04f-481b-9c5a-4e2ca879b54e" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.

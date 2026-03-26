# OPENING--AND-CLOSING
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
Use Closing operation

 
## Program:

### NAME : Susindhar K M
### REF NO : 212223040218
```
# Import libraries
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Read image in grayscale
image = cv2.imread("rose.png", 0)

# Create structuring element (kernel)
kernel = np.ones((5,5), np.uint8)

# ---------------- OPENING ----------------
opening = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# ---------------- CLOSING ----------------
closing = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

# ---------------- DISPLAY OUTPUT ----------------
titles = ["Original Image", "Opening", "Closing"]
images = [image, opening, closing]

plt.figure(figsize=(10,5))

for i in range(3):
    plt.subplot(1,3,i+1)
    plt.imshow(images[i], cmap='gray')
    plt.title(titles[i])
    plt.axis("off")

plt.tight_layout()
plt.show()
```
## Output:

### Display the input Image
<img width="418" height="581" alt="Screenshot 2026-03-26 143126" src="https://github.com/user-attachments/assets/3ffe377c-b997-4106-a8b6-f3a8675affed" />


### Display the result of Opening
<img width="414" height="581" alt="Screenshot 2026-03-26 143132" src="https://github.com/user-attachments/assets/95092760-ed7a-4dd6-94c4-3d475ca4080a" />


### Display the result of Closing
<img width="413" height="579" alt="Screenshot 2026-03-26 143138" src="https://github.com/user-attachments/assets/4828c7f2-7370-4913-861d-120c204d267d" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.

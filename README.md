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
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Read image in grayscale
image = cv2.imread("Italy P1.jpg", 0)

if image is None:
    print("Image not found!")
else:
    plt.imshow(image, cmap='gray')
    plt.title("Original Image")
    plt.axis("off")
    plt.show()


# Create structuring element
kernel = np.ones((5, 5), np.uint8)

# Perform Opening
opening = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# Display output
plt.imshow(opening, cmap='gray')
plt.title("Opening Image")
plt.axis("off")
plt.show()


# Create structuring element
kernel = np.ones((5, 5), np.uint8)

# Perform Closing
closing = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

# Display output
plt.imshow(closing, cmap='gray')
plt.title("Closing Image")
plt.axis("off")
plt.show()


```
## Output:

### Display the input Image
<img width="761" height="455" alt="image" src="https://github.com/user-attachments/assets/42ba8b52-92b1-4dc5-a76b-a50927536e9f" />



### Display the result of Opening
<img width="872" height="446" alt="image" src="https://github.com/user-attachments/assets/6d1bd030-1c12-44f9-8e2a-4a22c583a7eb" />


### Display the result of Closing
<img width="764" height="448" alt="image" src="https://github.com/user-attachments/assets/3101e903-8b06-49d4-98b6-f456647ffd9d" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.

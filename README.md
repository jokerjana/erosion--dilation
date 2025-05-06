# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Create a blank image.

### Step2:
Create a structuring element (5x5 rectangular)

### Step3:
Erode the image.

### Step4:
Dilate the image.

### Step5:
End the program.

 
## Program:

```
# Developed By: JANARTHANAN B
# Register No: 212223100014

import cv2
import numpy as np
import matplotlib.pyplot as plt


image = np.zeros((500, 500, 3), dtype=np.uint8)


font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'JANARTHANAN B', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)


plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')


kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)

plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')

dilated_image = cv2.dilate(image, kernel, iterations=1)


plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Dilated Image")
plt.axis('off')
```
## Output:

### Display the input Image:
![Screenshot 2025-05-06 134727](https://github.com/user-attachments/assets/05d2ae14-6c30-40de-bf29-2c4608c4f9ef)





### Display the Eroded Image:
![Screenshot 2025-05-06 134740](https://github.com/user-attachments/assets/e4772ea8-1704-4874-80d6-7a71fe19e877)




### Display the Dilated Image:
![Screenshot 2025-05-06 134752](https://github.com/user-attachments/assets/6488582e-3402-49f6-addc-a9dc14fd0f7e)





## Result
Thus the generated text image is eroded and dilated using python and OpenCV.

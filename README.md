# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

### Step1:
<br> import the neccesary packages


### Step2:
<br> creat the text using cv2.put Text

### Step3:
<br> create the structuting element

### Step4:
<br>  Erodde the image

### Step5:
<br> Dilate the image

 
## Program:

``` Python


import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((500, 500, 3), dtype=np.uint8)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Hello World', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
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

### Display the input Image
![image](https://github.com/user-attachments/assets/0c3d2a69-1434-479d-9b2e-232f3ea23d4e)


### Display the Eroded Image
![image](https://github.com/user-attachments/assets/f0ab8fb3-9229-47ad-bf3d-f049d7521ffa)


### Display the Dilated Image
![image](https://github.com/user-attachments/assets/b4c0212d-8f3c-429d-b201-1f9f3f1c7239)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.

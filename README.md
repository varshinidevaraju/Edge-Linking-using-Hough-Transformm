# Edge-Linking-using-Hough-Transformm
## Aim:
To write a Python program to detect the lines using Hough Transform.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import all the necessary modules for the program.
### Step2:

Load a image using imread() from cv2 module.
### Step3:

Convert the image to grayscale.
### Step4:

Using Canny operator from cv2,detect the edges of the image.
### Step5:

Using the HoughLinesP(),detect line co-ordinates for every points in the images.Using For loop,draw the lines on the found co-ordinates.Display the image.

## PROGRAM:

## DEVELOPED BY: VARSHINI D
## REG NO : 212223230234
```

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('carrom.png')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
edges = cv2.Canny(gray_image, 50, 150, apertureSize=3)
output_image = image.copy()
if lines is not None:
    for line in lines:
        x1, y1, x2, y2 = line[0]
        cv2.line(output_image, (x1, y1), (x2, y2), (0, 255, 0), 2)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Input Image')
plt.axis('off')
plt.show()
plt.imshow(gray_image, cmap='gray')
plt.title('Grayscale Image')
plt.axis('off')
plt.show()
plt.imshow(edges, cmap='gray')
plt.title('Canny Edge Detector Output')
plt.axis('off')
plt.show()
plt.imshow(cv2.cvtColor(output_image, cv2.COLOR_BGR2RGB))
plt.title('Hough Transform - Line Detection')
plt.axis('off')
plt.show()
```
## Output

### Input image and grayscale image
![image](https://github.com/user-attachments/assets/1276fce2-1bd2-44de-8bbc-87da69c04597)
![image](https://github.com/user-attachments/assets/a5c76408-c1fa-412f-96ab-4cfe71b6c0ac)


### Canny Edge detector output
![image](https://github.com/user-attachments/assets/782a4f74-991f-44ea-8f8d-0652ba1eaaf4)



### Display the result of Hough transform
![image](https://github.com/user-attachments/assets/0fa454af-38f6-4805-8d7d-68dda1ce2061)

## Result:
Hence, a python program to detect the lines using Hough Transform is implemented and executed.

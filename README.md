# EX-7 EDGEDETECTION
### Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors. &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;**DATE:** 27.09.2023
### Software Required:
Anaconda - Python 3.7
### Algorithm:
- Step1: Import the require libraries.
- Step2: Read the image and convert the bgr image to gray scale image.
- Step3: Apply various filter methods.
- Step4: Display the Output Images.
- Step5: End the Program.
```
Developed By: SHALINI K
Register No: 212222240095
```
### Program:
- Import packages and load image.
```Python
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("exp5.jpg")
gray = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
gray = cv2.GaussianBlur(gray,(3,3),0)
plt.title("Original Gray image")
plt.imshow(gray,cmap='gray')
plt.axis('off')
plt.show()
```
- Sobel Edge Detector
  - Sobel X:
    ```Python
    sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
    plt.imshow(sobelx,cmap='gray')
    plt.title("Sobel X axis")
    plt.axis("off")
    plt.show()
    ```
  - Sobel Y:
    ```Python
    sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
    plt.imshow(sobely,cmap='gray')
    plt.title("Sobel Y axis")
    plt.axis("off")
    plt.show()
    ```
  - Sobel XY:
    ```Python
    sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
    plt.imshow(sobelxy,cmap='gray')
    plt.title("Sobel XY axis")
    plt.axis("off")
    plt.show()
    ```
- Laplacian Edge Detector:
  ```Python
  lap=cv2.Laplacian(gray,cv2.CV_64F)
  plt.imshow(lap,cmap='gray')
  plt.title("Laplacian Edge Detector")
  plt.axis("off")
  plt.show()
  ``` 
- Canny Edge Detector:
  ```Python
  canny=cv2.Canny(gray,120,150)
  plt.imshow(canny,cmap='gray')
  plt.title("Canny Edge Detector")
  plt.axis("off")
  plt.show()
  ```
### Output:
<img height=20% width=30% src="https://github.com/shalinikannan23/EDGE-DETECTION/assets/118656529/aad28483-049e-477b-b957-c46cd845f541">
<img height=20% width=30% src="">
<img height=20% width=30% src="">
<img height=20% width=30% src="https://github.com/ROHITJAIND/EDGE-DETECTION/assets/118707073/8f94f92d-0e30-4e44-b1df-4de7c9615a26">
<img height=20% width=30% src="https://github.com/ROHITJAIND/EDGE-DETECTION/assets/118707073/73bca070-b7c4-45ca-b98f-99b79671cff5">
<img height=20% width=30% src="https://github.com/ROHITJAIND/EDGE-DETECTION/assets/118707073/f93201e7-0c5c-416e-869a-2413b60b77e7">  

### Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

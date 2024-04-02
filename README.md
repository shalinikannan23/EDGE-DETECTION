# EX-6 EDGE DETECTION
### Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors. &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;**DATE:** 02.04.2024
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
<img height=20% width=30% src="https://github.com/shalinikannan23/EDGE-DETECTION/assets/118656529/768ca4f9-2f35-4f56-9f9a-cd77957fc3a2">
<img height=20% width=30% src="https://github.com/shalinikannan23/EDGE-DETECTION/assets/118656529/8f86c61e-54c1-449c-8766-246d6deccb76">
<img height=20% width=30% src="https://github.com/shalinikannan23/EDGE-DETECTION/assets/118656529/385ce5a7-27e1-4bc3-a909-87522df5681d">
<img height=20% width=30% src="https://github.com/shalinikannan23/EDGE-DETECTION/assets/118656529/2a2cac65-1600-4209-8e70-11a7f57f6e30">
<img height=20% width=30% src="https://github.com/shalinikannan23/EDGE-DETECTION/assets/118656529/cbdd9d3d-d6de-495e-a1f5-9f47cbbfd182">
<img height=20% width=30% src="https://github.com/shalinikannan23/EDGE-DETECTION/assets/118656529/be568c1c-1dbf-4177-8042-b32d08620c40">  

### Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

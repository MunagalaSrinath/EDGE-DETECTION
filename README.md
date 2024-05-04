# EX-6 EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.
### Step2:
Load a image using imread() from cv2 module.
### Step3:
Convert the image to grayscale
### Step4:
Using Sobel operator from cv2,detect the edges of the image.
### Step5:
Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## PROGRAM:
```
DEVELOPED BY: M SRINATH
REGISTER NUMBER: 212222230147
```
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("elon.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
**SOBEL X:**
  ```python
  sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y:**
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY:**
  ```python
  sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LAPLACIAN EDGE DETECTOR:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## ORIGINAL IMAGE:
![image](https://github.com/MunagalaSrinath/EDGE-DETECTION/assets/118678482/402c02fb-45a7-411e-b363-1c422f498241)

### SOBEL EDGE DETECTOR:
![image](https://github.com/MunagalaSrinath/EDGE-DETECTION/assets/118678482/d989f111-716a-4f8e-8a9a-41d0452b97e6)
![image](https://github.com/MunagalaSrinath/EDGE-DETECTION/assets/118678482/50d72c64-5ddf-40c4-9a7e-f0bc4edad8e7)
![image](https://github.com/MunagalaSrinath/EDGE-DETECTION/assets/118678482/6b2984dd-2e74-4e1c-9bfe-66ad16e59887)
### LAPLACIAN EDGE DETECTOR
![image](https://github.com/MunagalaSrinath/EDGE-DETECTION/assets/118678482/1969155f-803e-4bc2-bc2e-0ce325e9a506)
### CANNY EDGE DETECTOR
![image](https://github.com/MunagalaSrinath/EDGE-DETECTION/assets/118678482/6e038472-3cac-43ce-a057-f9fcfe98bf83)
## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

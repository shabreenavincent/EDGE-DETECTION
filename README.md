# EDGE-DETECTION
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
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("edge.jpg",0)
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
![vk king](https://github.com/SHARAN-MJ/EDGE-DETECTION/assets/119560305/0afc89c1-0233-4463-8475-135a814869ca)

### SOBEL EDGE DETECTOR:
![Screenshot 2024-04-12 090139](https://github.com/SHARAN-MJ/EDGE-DETECTION/assets/119560305/955c988d-bd29-48d3-91c1-9ccede62d53f)
![Screenshot 2024-04-12 090147](https://github.com/SHARAN-MJ/EDGE-DETECTION/assets/119560305/313771a5-0c2d-445f-939d-fe4937dbb2f2)
![Screenshot 2024-04-12 090154](https://github.com/SHARAN-MJ/EDGE-DETECTION/assets/119560305/309f96e3-2da6-4c18-9945-31428e6354c6)

### LAPLACIAN EDGE DETECTOR
![Screenshot 2024-04-12 090200](https://github.com/SHARAN-MJ/EDGE-DETECTION/assets/119560305/e329ad9f-e854-4cc1-b6fa-1f700472d736)

### CANNY EDGE DETECTOR
![Screenshot 2024-04-12 090209](https://github.com/SHARAN-MJ/EDGE-DETECTION/assets/119560305/e075e76e-fe11-4aab-902a-e3e8cdb115aa)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

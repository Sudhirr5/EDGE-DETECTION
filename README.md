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

## Program:
```
Developed by : SUDHIR KUMAR. R
Register number : 212223230221
```

```python
import cv2
import matplotlib.pyplot as plt

img = cv2.imread(r"C:\Users\admin\dig-img-process\fie.jpg")
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
gray = cv2.GaussianBlur(gray, (3, 3), 0)

sobelx = cv2.Sobel(gray, cv2.CV_64F, 1, 0, ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 2, 2)
plt.imshow(sobelx, cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()

sobely = cv2.Sobel(gray, cv2.CV_64F, 0, 1, ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 2, 2)
plt.imshow(sobely, cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()

sobelxy = cv2.Sobel(gray, cv2.CV_64F, 1, 1, ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 2, 2)
plt.imshow(sobelxy, cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()

lap = cv2.Laplacian(gray, cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 2, 2)
plt.imshow(lap, cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()

canny = cv2.Canny(gray, 120, 150)
plt.figure(figsize=(8,8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 2, 2)
plt.imshow(canny, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()

```
## Output:
### SOBEL EDGE DETECTOR

![Screenshot 2024-09-30 161757](https://github.com/user-attachments/assets/c2bd4c9d-84d0-4baa-b4a7-6eef1e14fe5d)

![Screenshot 2024-09-30 161812](https://github.com/user-attachments/assets/fcb36263-fc7a-4b44-ad7b-81b4de426208)

![Screenshot 2024-09-30 161824](https://github.com/user-attachments/assets/f412e463-4e91-48b4-aa4b-d2de7f187a47)

### LAPLACIAN EDGE DETECTOR

![Screenshot 2024-09-30 161836](https://github.com/user-attachments/assets/c162a132-be5e-4ef0-9030-b79986bc4868)

### CANNY EDGE DETECTOR

![Screenshot 2024-09-30 161851](https://github.com/user-attachments/assets/69b7da95-98a3-499e-8126-7466c320b93d)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

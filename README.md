# EDGE-DETECTION
# Name: MOHAMMAD FAIZAL SK
# Register No: 212223240092
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

## Output:
### SOBEL EDGE DETECTOR
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('rome.png')
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
gray = cv2.GaussianBlur(gray, (3, 3), 0)
sobelx = cv2.Sobel(gray, cv2.CV_64F, 1, 0, ksize=5)
plt.figure(figsize=(8, 8))
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

plt.figure(figsize=(8, 8))
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

plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobelxy, cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()

```
<img width="831" height="303" alt="image" src="https://github.com/user-attachments/assets/561cc5b8-e513-4cc7-9e92-237efebc9bc4" />
<img width="830" height="302" alt="image" src="https://github.com/user-attachments/assets/89b0390a-4eac-4f12-8c7b-b046b5202dd7" />
<img width="823" height="298" alt="image" src="https://github.com/user-attachments/assets/92b10172-29be-4d47-8fc2-1fb7013b047a" />

### LAPLACIAN EDGE DETECTOR
```
    lap = cv2.Laplacian(gray, cv2.CV_64F)
    
    plt.figure(figsize=(8, 8))
    plt.subplot(1, 2, 1)
    plt.imshow(gray, cmap='gray')
    plt.title("Original Image")
    plt.axis("off")
    plt.subplot(1, 2, 2)
    plt.imshow(lap, cmap='gray')
    plt.title("Laplacian Edge Detector")
    plt.axis("off")
    plt.show()

```
<img width="875" height="309" alt="image" src="https://github.com/user-attachments/assets/12e5a5bc-7a44-420f-a07f-e79945fac970" />

### CANNY EDGE DETECTOR
```
canny = cv2.Canny(gray, 120, 150)

plt.figure(figsize=(8, 8))
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
<img width="836" height="289" alt="image" src="https://github.com/user-attachments/assets/f13aff43-b499-4fc8-a947-45d08caac173" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

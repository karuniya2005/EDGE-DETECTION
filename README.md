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
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("q1.png") 

# CONVERT THE COLOR TO GRAY 
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Apply Gaussian Blur
gray = cv2.GaussianBlur(gray, (3, 3), 0)

# Sobel X
sobelx = cv2.Sobel(gray, cv2.CV_64F, 1, 0, ksize=5)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap="gray")
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobelx, cmap="gray")
plt.title("Sobel X axis")
plt.axis("off")
plt.show()

# Sobel Y
sobely = cv2.Sobel(gray, cv2.CV_64F, 0, 1, ksize=5) 
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap="gray")
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobely, cmap="gray")
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()

# Sobel XY
sobelxy = cv2.Sobel(gray, cv2.CV_64F, 1, 1, ksize=5)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap="gray")
plt.title("Original Image")
plt.axis("off")
# DISPLAY THE SOBEL XY
plt.subplot(1, 2, 2)
plt.imshow(sobelxy, cmap="gray")
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()

# Laplacian
lap = cv2.Laplacian(gray, cv2.CV_64F)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap="gray")
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(lap, cmap="gray")   # <-- filled missing code
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()

# Canny
canny = cv2.Canny(gray, 120, 150)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap="gray")
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(canny, cmap="gray")
plt.title("Canny Edge Detector")   
plt.axis("off")
plt.show()

```

## Output:
### SOBEL EDGE DETECTOR

<img width="454" height="765" alt="image" src="https://github.com/user-attachments/assets/f019e6e5-c7fd-4ec0-8b91-efcedff9668e" />


### LAPLACIAN EDGE DETECTOR

<img width="610" height="383" alt="image" src="https://github.com/user-attachments/assets/9aad4d84-a31e-4497-ae31-2e9beb2902c8" />


### CANNY EDGE DETECTOR

<img width="635" height="424" alt="image" src="https://github.com/user-attachments/assets/d78537c0-4f38-4081-b1df-93452dac7481" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

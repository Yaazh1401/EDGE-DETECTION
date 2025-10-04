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

## Output:
### SOBEL EDGE DETECTOR

```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("C:\\Users\\admin\\OneDrive\\Desktop\\DIPT\\bunny.jpeg")
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



<img width="959" height="432" alt="image" src="https://github.com/user-attachments/assets/fc2b4aed-0226-4a4b-a7bc-2b6817b8f79b" />


<img width="950" height="426" alt="image" src="https://github.com/user-attachments/assets/7302b9f3-216f-4d5f-b4bb-b313eeb896b3" />


<img width="1001" height="427" alt="image" src="https://github.com/user-attachments/assets/c528f31e-1cff-481b-a45c-7fe23a53bf5f" />




### LAPLACIAN EDGE DETECTOR

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



<img width="1022" height="404" alt="image" src="https://github.com/user-attachments/assets/f4c17a44-fe2b-4837-b918-3163a56a3b06" />



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


<img width="922" height="424" alt="image" src="https://github.com/user-attachments/assets/b8da772e-d89b-41a2-b57b-e2d37ffe0ecf" />



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

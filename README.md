# CANNY-EDGE-DETECTION
## Aim:
To perform Canny edge detection algorithm and obtain the edges with different parameter settings.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
Step1:

To perform edge detection using Canny edge detectors.

Step2:

For performing edge detection on a image.
Canny : canny_edges=cv2.Canny(gray,50,150)

For different parameters :

i) Low thresholds (detects more edges, including noise) : canny_edges1 = cv2.Canny(blurred, 30, 80)

ii) Balanced thresholds (good trade-off) : canny_edges2 = cv2.Canny(blurred, 50, 100)

iii)High thresholds (detects only strong edges) : canny_edges3 = cv2.Canny(blurred, 100, 200)

Step3:

Display all the images with their respective edge detected images.

## Program :
### Name : Dharshni V M
### Register Number: 212223240029
```
import cv2
import matplotlib.pyplot as plt

image = cv2.imread('ocean.png') 
gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

blurred = cv2.GaussianBlur(gray, (5, 5), 1.4)
canny_edges = cv2.Canny(gray, 50, 150)

plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.title('Original Image')
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.axis('off')
plt.show()

plt.figure(figsize=(8,8))
plt.subplot(1, 2, 2)
plt.title('Canny Edge Detection')
plt.imshow(canny_edges, cmap='gray')
plt.axis('off')
plt.show()

canny_edges1 = cv2.Canny(blurred, 30, 80)
plt.figure(figsize=(8, 8))
plt.subplot(2, 2, 2)
plt.title('Canny Low Thresholds')
plt.imshow(canny_edges1, cmap='gray')
plt.axis('off')
plt.show()

canny_edges2= cv2.Canny(blurred, 50, 100)
plt.figure(figsize=(8, 8))
plt.subplot(2, 2, 3)
plt.title('Canny Balanced Thresholds')
plt.imshow(canny_edges2, cmap='gray')
plt.axis('off')
plt.show()

canny_edges3 = cv2.Canny(blurred, 100, 200)
plt.figure(figsize=(8,8))
plt.subplot(2, 2, 4)
plt.title('Canny High Thresholds')
plt.imshow(canny_edges3, cmap='gray')
plt.axis('off')

plt.tight_layout()
plt.show()
```
## Output:
### Original Image:
![original](https://github.com/user-attachments/assets/7d0d8503-7acc-4975-9739-0909b3f7a657)

### Canny Edge Detection:
![canny](https://github.com/user-attachments/assets/a2a3fbb9-d89f-4d33-805d-c62c5160be33)

### Canny Low Thresholds:
![canny low](https://github.com/user-attachments/assets/875a3eef-0a49-4603-a3e5-f3b9342398e1)

### Canny Balanced Thresholds:
![canny balanced](https://github.com/user-attachments/assets/f0397400-c1f1-4e71-87b9-ae5698556cb7)

### Canny High Thresholds:
![canny high](https://github.com/user-attachments/assets/5a43a6b3-b0f2-4366-9a22-9210055f3322)

## Result:
Thus , the edges are detected by Canny edge detection and also implemented with different parameter settings.

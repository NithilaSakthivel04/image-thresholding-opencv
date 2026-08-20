# Image Segmentation Using Thresholding Techniques in OpenCV

## Aim

To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

- Global Thresholding
- Adaptive Thresholding
- Otsu's Thresholding

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Load the input image using OpenCV.

### Step 3:

Convert the input image into grayscale format.

### Step 4: Global Thresholding

- Select a fixed threshold value.
- Apply thresholding to separate foreground and background pixels.
- Display the thresholded image.

### Step 5: Adaptive Thresholding

- Compute threshold values for small regions of the image.
- Apply Adaptive Mean Thresholding.
- Apply Adaptive Gaussian Thresholding.
- Display the segmented images.

### Step 6: Otsu's Thresholding

- Automatically determine the optimal threshold value.
- Apply Otsu's thresholding technique.
- Display the segmented image.

### Step 7:

Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

## Program
## Import Libraries
```
import cv2
import matplotlib.pyplot as plt
```
## Read the Image
```
image = cv2.imread(r"C:\Users\admin\puppy.png")

if image is None:
    print("Image not found. Check path.")
else:
    print("Image loaded successfully.")
```
## Convert to Grayscale
```
gray_img = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

```
## Display Original Image
```
plt.subplot(2,2,1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
```
## Global Thresholding
```
_, global_thresholded = cv2.threshold(
    gray_img, 127, 255, cv2.THRESH_BINARY
)
adaptive_thresholded = cv2.adaptiveThreshold(
    gray_img,
    255,
    cv2.ADAPTIVE_THRESH_GAUSSIAN_C,
    cv2.THRESH_BINARY,
    11,
    2
)
_, otsu_thresholded = cv2.threshold(
    gray_img,
    0,
    255,
    cv2.THRESH_BINARY + cv2.THRESH_OTSU
)
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```
## Adaptive Thresholding
```

plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```
## Otsu's Thresholding
```
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
```

## Developed By

**Name:** NITHILA S

**Register No:** 212224040224
## Output

### Original Grayscale Image

<img width="192" height="280" alt="image" src="https://github.com/user-attachments/assets/d76bf52a-3200-4cea-8041-b482766ee387" />


### Global Thresholding

<img width="243" height="285" alt="image" src="https://github.com/user-attachments/assets/9fc1ca1a-052a-4ae8-b2ed-8c924e23dfaf" />


### Adaptive Thresholding


<img width="271" height="286" alt="image" src="https://github.com/user-attachments/assets/e0e0ae5e-3eb8-4ba3-bc79-185dcfdbe03b" />


### Otsu's Thresholding


<img width="198" height="278" alt="image" src="https://github.com/user-attachments/assets/69c0fb23-3f7f-411f-8529-26ad74277757" />



<img width="906" height="942" alt="image" src="https://github.com/user-attachments/assets/be1242d2-fe57-4dc8-a6dc-af836bf092b6" />



## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 

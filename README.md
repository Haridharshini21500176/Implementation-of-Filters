# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries and read the image.

### Step 2:
Convert the saved BGR image to RGB using cvtColor().

### Step 3:
Use the filters required for image smoothing and sharpening.

### Step 4:
Apply the filters using cv2.filter2D() for each respective filters.

### Step 5:
Plot the images of the original one and the filtered one using plt.figure() and cv2.imshow(). 


## Program:
### Developed By   :HARIDHARSHINI.S
### Register Number:212221230033
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
kernel1 = np.ones((11,11),np.float32)/121
avg_filter = cv2.filter2D(original_image,-1,kernel1)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(avg_filter)
plt.title("Filtered")
plt.axis("off")

```
ii) Using Weighted Averaging Filter
```Python
kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weighted_filter = cv2.filter2D(original_image,-1,kernel2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(weighted_filter)
plt.title("Filtered")
plt.axis("off")

```
iii) Using Gaussian Filter
```Python
gaussian_blur = cv2.GaussianBlur(src = original_image, ksize = (11,11), sigmaX=0, sigmaY=0)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Filtered")
plt.axis("off")

```

iv) Using Median Filter
```Python
median = cv2.medianBlur(src=original_image,ksize = 11)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Filtered")
plt.axis("off")

```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(original_image,-1,kernel3)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_kernel)
plt.title("Filtered")
plt.axis("off")

```
ii) Using Laplacian Operator
```Python
laplacian_operator = cv2.Laplacian(original_image,cv2.CV_64F)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_operator)
plt.title("Filtered")
plt.axis("off")

```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>
![ex 6 a](https://user-images.githubusercontent.com/94168395/230025527-cac3fed5-a306-4ea2-927a-42e887f99d7e.png)

ii) Using Weighted Averaging Filter

![ex 6 b](https://user-images.githubusercontent.com/94168395/230025587-53801ff8-67ac-4ad5-8b39-0485de67f0f2.png)

iii) Using Gaussian Filter


![ex 6 c](https://user-images.githubusercontent.com/94168395/230025753-3bcf6c26-d1ea-46da-ab64-bcad35a4f97b.png)

iv) Using Median Filter

![ex 6 d](https://user-images.githubusercontent.com/94168395/230025927-cef15042-7b72-4a4c-bf87-e8da82d1a92e.png)

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
![ex 6 e](https://user-images.githubusercontent.com/94168395/230026006-3fd0ab7d-bb52-4087-9a50-3b02b0872210.png)


ii) Using Laplacian Operator

![ex 6 f](https://user-images.githubusercontent.com/94168395/230026049-9ca37855-fce1-47b4-8d8c-81fab5d21f11.png)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.

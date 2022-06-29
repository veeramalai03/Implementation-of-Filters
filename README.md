## Ex no: 6
## Date: 03/05/2022
# <p align="center">Implementation-of-filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the necessary modules.

### Step2
For performing smoothing operation on a image.
```python
avg_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
```
Weighted average filter
```python
wt_avg_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
wt_average_filter_image=cv2.filter2D(image,-1,wt_avg_kernel)
```
Gaussian Blur
```python
gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
```
Median filter
```python
median_blur=cv2.medianBlur(image,11)
```

### Step3
For performing sharpening on a image.

Laplacian Kernel
```python
lap_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
lap_image=cv2.filter2D(image,-1,lap_kernel)
```
Laplacian Operator
```python
Lap_sharp=cv2.Laplacian(image,cv2.CV_64F)
```

### Step4
Display all the images with their respective filters.

## Program:
### Developed By   : VEERAMALAI S
### Register Number: 212220230056
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
avg_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Average Filter image')
plt.imshow(average_filter_image)
plt.show()



```
ii) Using Weighted Averaging Filter
```Python
weight_average_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weight_average_filter_image=cv2.filter2D(image,-1,weight_average_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image[30:200,50:200])
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Weighted average Filter image')
plt.imshow(weight_average_filter_image[30:200,50:200])
plt.show()



```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Gaussian Filter image')
plt.imshow(gaussian_blur)
plt.show()



```

iv) Using Median Filter
```Python
median_blur=cv2.medianBlur(image,11)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Median Filter image')
plt.imshow(median_blur)
plt.show()




```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
laplacian_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
laplacian_image=cv2.filter2D(image,-1,laplacian_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian Kernel Filter image')
plt.imshow(laplacian_image)
plt.show()




```
ii) Using Laplacian Operator
```Python
Laplacian_sharp=cv2.Laplacian(image,cv2.CV_64F)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian Operator Filter image')
plt.imshow(Laplacian_sharp)
plt.show()




```

## OUTPUT:
![dip-6-1](https://user-images.githubusercontent.com/75235601/167667464-948e0b98-9905-49da-bb1d-744bf2ddbd67.jpg)

### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>![dip-6-2](https://user-images.githubusercontent.com/75235601/167667847-3c08786f-8cbc-4054-8f5a-803ece834f03.jpg)

ii) Using Weighted Averaging Filter
</br>![dip-6-3](https://user-images.githubusercontent.com/75235601/167667966-3e309de6-f22c-4b67-ac30-7dcf5b888812.jpg)


iii) Using Gaussian Filter
</br>![dip-6-4](https://user-images.githubusercontent.com/75235601/167668346-42c373fc-d296-42cd-816c-b54890bb25c7.jpg)


iv) Using Median Filter
</br>![dip-6-5](https://user-images.githubusercontent.com/75235601/167668395-1362c9c9-f01b-40f3-83f1-f8b1b61fe313.jpg)


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>![dip-6-6](https://user-images.githubusercontent.com/75235601/167668457-b2edb15b-199d-4c4c-abd2-6647e4e06652.jpg)


ii) Using Laplacian Operator
</br>![dip-6-7](https://user-images.githubusercontent.com/75235601/167668499-142e54e3-a883-42a4-82de-655ac1b35149.jpg)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.

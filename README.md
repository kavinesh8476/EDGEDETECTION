# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>
Import the required packages for further process.
<br>

### Step2:
<br>
Read the image and convert the bgr image to gray scale image.
<br>

### Step3:
<br>
Use any filters for smoothing the image to reduse the noise.
<br>

### Step4:
<br>
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.
<br>

### Step5:
<br>
Display the filtered image using plot and imshow.
<br>

## Program:
```
DEVELOPED BY : Kavinesh M
REG NO : 212222230064
```


### Import the packages
```
import cv2
import matplotlib.pyplot as plt
```

### Load the image, Convert to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("windows.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```


### SOBEL EDGE DETECTOR
### SOBEL X AXIS :
```
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
### SOBEL Y AXIS :
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
### SOBEL XY AXIS :
```
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```

# LAPLACIAN EDGE DETECTOR
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```


### CANNY EDGE DETECTOR
```
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:
### SOBEL EDGE DETECTOR
### SOBEL X AXIS :
<br>

![image](https://github.com/kavinesh8476/EDGEDETECTION/assets/118466561/622b15d6-7748-4723-b542-36fcf77752df)

<br>

### SOBEL Y AXIS :
<br>

![image](https://github.com/kavinesh8476/EDGEDETECTION/assets/118466561/8066bc7b-74eb-47f5-b54c-51551af23570)


<br>

### SOBEL XY AXIS :
<br>

![image](https://github.com/kavinesh8476/EDGEDETECTION/assets/118466561/182a2ebb-a022-4744-a1b2-1b1928cc68e2)

<br>

### LAPLACIAN EDGE DETECTOR
<br>

![image](https://github.com/kavinesh8476/EDGEDETECTION/assets/118466561/fbd48718-5a64-4bbf-8fa0-e4fc2d00a724)

<br>



### CANNY EDGE DETECTOR
<br>

![image](https://github.com/kavinesh8476/EDGEDETECTION/assets/118466561/3f0d56ce-7626-4556-b4d7-6b0ee0423e53)

<br>


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

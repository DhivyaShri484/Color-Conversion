# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:

import opencv.
<br>

### Step2:

Read the original Image.
<br>

### Step3:

Store the required conversion of the image in a variable.
<br>

### Step4:

Show the image stored in the given variable.
<br>

### Step5:

Destroy all the windows and end the program.
<br>

## Program:
```python
# Developed By: Dhivya Shri
# Register Number: 212221230009
# i) Convert BGR and RGB to HSV and GRAY

import cv2
Image = cv2.imread('dip.jpeg')
cv2.imshow('Original Image',Image)
hsvImage = cv2.cvtColor(Image,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsvImage)
hsvImage1=cv2.cvtColor(Image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvImage1)
grayImage = cv2.cvtColor(Image,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',grayImage)
grayImage1 = cv2.cvtColor(Image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayImage1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```

# ii)Convert HSV to RGB and BGR

import cv2
HSVImage = cv2.imread('dip.jpeg')
cv2.imshow('Original HSV Image',HSVImage)
RGBImage = cv2.cvtColor(HSVImage,cv2.COLOR_HSV2RGB)
cv2.imshow('BGR2HSV',RGBImage)
BGRImage=cv2.cvtColor(HSVImage,cv2.COLOR_HSV2BGR)
cv2.imshow('RGB2HSV',BGRImage)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```
# iii)Convert RGB and BGR to YCrCb

import cv2
Image = cv2.imread('dip.jpeg')
cv2.imshow('Original HSV Image',Image)
YCrCb_image = cv2.cvtColor(Image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR2HSV',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(Image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2HSV',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```
# iv)Split and Merge RGB Image

import cv2
image = cv2.imread('dip.jpeg')
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
mergeBgr = cv2.merge((blue,green,red))
cv2.imshow('Merged BGR image',mergeBgr)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```
# v) Split and merge HSV Image

import cv2
image = cv2.imread('dip.jpeg')
hsv = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue - Image',h)
cv2.imshow('Saturation - Image',s)
cv2.imshow('Gray - Image',v)
mergedHSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',mergedHSV)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### i) BGR and RGB to HSV and GRAY
<br>
<img width="1361" alt="1" src="https://user-images.githubusercontent.com/94505585/228147736-caa5e83b-fa83-40f1-9981-c8793629094d.png">
<br>

### ii) HSV to RGB and BGR
<br>
<img width="1268" alt="2" src="https://user-images.githubusercontent.com/94505585/228149211-ee36f40e-533c-42eb-bd7a-1b083c0fec7e.png">
<br>

### iii) RGB and BGR to YCrCb
<br>
<img width="1225" alt="3" src="https://user-images.githubusercontent.com/94505585/228149266-de83cfd5-b7ad-472f-94da-f23f1744e008.png">
<br>

### iv) Split and merge RGB Image
<br>
<img width="1345" alt="4" src="https://user-images.githubusercontent.com/94505585/228149443-e868ebec-7c39-4ff1-9054-f6aed2627a33.png">
<br>

### v) Split and merge HSV Image
<br>
<img width="1125" alt="5" src="https://user-images.githubusercontent.com/94505585/228149534-669aa460-c4cf-4b06-9731-5a765f366da3.png">
<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.

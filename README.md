# Color Conversion
## AIM:
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## ALGORITHM:
### Step 1:
Read an image using imread() and
Convert BGR and RGB to HSV and GRAY<br/>
using:<br/>cv2.cvtColor(image,cv2.COLOR_RGB2HSV)<br/>cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)<br/>cv2.cvtColor(image,cv2.COLOR_BGR2HSV)<br/>cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)<br/>
### Step 2:
Convert HSV to RGB and BGR<br/>
using:<br/>
cv2.cvtColor(image,cv2.COLOR_HSV2RGB)<br/>
cv2.cvtColor(image,cv2.COLOR_HSV2BGR)<br/>
### Step 3:
Convert RGB and BGR to YCrCb<br/>
using:<br/>cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)<br/>cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)<br/>
### Step 4:
Split and Merge RGB Image
<br>using:<br/>blue = image[:,:,0]<br/>green = image[:,:,1]<br/>red = image[:,:,2]<br/>cv2.merge((blue,green,red))<br/>
### Step 5:
Split and merge HSV Image
<br>using:<br/>hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)<br/>h, s, v = cv2.split(hsv)<br/>cv2.merge((h,s,v))<br/>

## PROGRAM:
```
# Developed By: Graham Stanes
# Register Number: 212220230020
# i) Convert BGR and RGB to HSV and GRAY

import cv2
image=cv2.imread("sample.jpg")
BGR_HSV=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("BGR to HSV image",BGR_HSV)
BGR_GRAY=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow("BGR to GRAY image",BGR_GRAY)
cv2.imshow("212220230020",image)
cv2.waitKey(0)
cv2.destroyAllWindows()

RGB_HSV=cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow("RGB to HSV image",RGB_HSV)
RGB_GRAY=cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow("RGB to GRAY image",RGB_GRAY)
cv2.imshow("212220230020",image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# ii)Convert HSV to RGB and BGR

hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("HSV image",hsv)
HSV_RGB=cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
cv2.imshow("HSV to RGB image",HSV_RGB)
HSV_BGR=cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow("HSV to BGR image",HSV_BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iii)Convert RGB and BGR to YCrCb

RGB_YCrCb=cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.imshow("RGB to YCrCb image",RGB_YCrCb)
BGR_YCrCb=cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR to YCrCb image",BGR_YCrCb)
cv2.imshow("212220230020",image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iv)Split and Merge RGB Image

blue = image[:,:,0]
cv2.imshow("Blue Split",blue)
green = image[:,:,1]
cv2.imshow("Green Split",green)
red = image[:,:,2]
cv2.imshow("Red Split",red)
merged=cv2.merge((blue,green,red))
cv2.imshow("Merged Image",merged)
cv2.imshow("212220230020",image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# v) Split and merge HSV Image

hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)
cv2.imshow('h_plane', h)
cv2.imshow('s_plane', s)
cv2.imshow('v_plane', v)
mergedhsv=cv2.merge((h,s,v))
cv2.imshow("HSV image",hsv)
cv2.imshow('Merged HSV',mergedhsv)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## OUTPUT:

### i) BGR and RGB to HSV and GRAY
![img1](https://user-images.githubusercontent.com/75235150/165338314-71fa01f1-15e7-4b98-96d7-077d4eaa01ba.jpg)
![img2](https://user-images.githubusercontent.com/75235150/165338335-c931c23b-696a-4a28-9239-59096f197642.jpg)


### ii) HSV to RGB and BGR
![img3](https://user-images.githubusercontent.com/75235150/165338371-a54aff85-eaeb-46e2-a3e7-ae73e8439c51.jpg)


### iii) RGB and BGR to YCrCb
![img4](https://user-images.githubusercontent.com/75235150/165338390-d842a640-1c4a-4e0b-b201-e1f7269a2332.jpg)


### iv) Split and merge RGB Image
![img5](https://user-images.githubusercontent.com/75235150/165338456-d2fdb627-1b08-46fb-bd16-21cddc0ad143.jpg)


### v) Split and merge HSV Image
![img6](https://user-images.githubusercontent.com/75235150/165338484-55c929ee-18a8-40d4-b2e3-4d4755948797.jpg)

## RESULT:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.

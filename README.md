# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 library and upload the image or capture an image.
### Step2:
Read the saved image using cv2.imread("filename.jpg").
### Step3:
Convert the image into the given color transformation using cv2.cvtColor(image, cv2.BGR2YCrCb) and similarly for other color formats.
### Step4:
Split and merge the image using cv2.split(hsv) and cv2.merge([h,s,v]).
### Step5:
Output the image using cv2.imshow("OUTPUT", image).

## Program:
```python
# Developed By:Dharmaraj S
# Register Number:212222240025

# i) Convert BGR and RGB to HSV and GRAY

import cv2
houseImage = cv2.imread('cheems.png')
cv2.imshow('Original Image',houseImage)
hsvImage = cv2.cvtColor(houseImage,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsvImage)
hsvImage1=cv2.cvtColor(houseImage,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvImage1)
grayImage = cv2.cvtColor(houseImage,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',grayImage)
grayImage1 = cv2.cvtColor(houseImage,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayImage1)
cv2.waitKey(0)
cv2.destroyAllWindows()


# ii)Convert HSV to RGB and BGR

import cv2
houseHSVImage = cv2.imread('cheems.png')
cv2.imshow('Original HSV Image',houseHSVImage)
RGBImage = cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2RGB)
cv2.imshow('BGR2HSV',RGBImage)
BGRImage=cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2BGR)
cv2.imshow('RGB2HSV',BGRImage)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iii)Convert RGB and BGR to YCrCb

import cv2
houseImage = cv2.imread('cheems.png')
cv2.imshow('Original HSV Image',houseImage)
YCrCb_image = cv2.cvtColor(houseImage, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR2HSV',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(houseImage, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2HSV',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()



# iv)Split and Merge RGB Image

import cv2
image = cv2.imread('cheems.png')
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



# v) Split and merge HSV Image

import cv2
image = cv2.imread('cheems.png')
hsv = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue - Image',h)
cv2.imshow('Saturation - Image',s)
cv2.imshow('Gray - Image',v)
mergedHSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',mergedHSV)
cv2.waitKey(0)
cv2.destroyAllWindow


```
## Output:
### i) BGR and RGB to HSV and GRAY

![original](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/3299ed65-db79-4689-ae02-c2846d96ee6b)
![BGR2HSV](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/7c8229bf-6bb5-4dc0-8837-2c154816f217)
![rgb2gray](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/7d58d36c-9601-4b46-a4ff-1197bf76b012)
![rgb2hsv](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/73b01b3a-9e1c-40eb-b8b8-2bda1cccfad1)
![bgr2gray](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/c1a76aa6-054c-416f-a245-bb8c860adf0f)

### ii) HSV to RGB and BGR

![original](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/f4c2516b-0bc6-42c0-bbfd-c93f3e50fff2)
![bgr](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/e2d57c8b-bb17-4fef-9ca0-780b9d8afffe)
![rgb](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/08ac38c2-3ff9-4576-941c-01ca477ba5ac)

### iii) RGB and BGR to YCrCb

![original](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/00e910a9-9202-47a9-98d6-902a33d12ff8)
![bgr](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/fd83efc0-3715-4e26-b4eb-52fff54df208)
![rgb](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/ac5258ad-0304-4d1e-9626-562cf0e4206e)

### iv) Split and merge RGB Image

![merged](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/824aad2a-e9a4-4b23-9b09-2a540dfb24c2)
![r](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/54540f9c-0baa-44b6-a622-a7bcee84f59b)
![g](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/f1928351-3abb-4b00-834f-6c35e449b83e)
![b](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/652ba2bc-6e09-47aa-b247-e38ac00d7cc5)

### v) Split and merge HSV Image

![mer](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/18e5f371-7dfb-465a-9900-dfcc509927cc)
![gray](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/ca742022-417f-4757-9ced-aed95a1a27d6)
![hure](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/2f978327-5ce3-4cbc-ba0c-15ed8d722252)
![sat](https://github.com/dharmaraj-007/COLOR-CONVERSION/assets/119560386/fcc402f1-4cef-4267-a5ba-c8bf18f430be)



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.

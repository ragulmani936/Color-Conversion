# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 and save an image as scolor.jpeg.

### Step2:
Use imread to read and display the image.

### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:
Split and merge the image using cv2.split and cv2.merge commands.

### Step5:
End the program and view the output image windows

## Program:
```python
# Developed By: Ragul M
# Register Number:212221230080
~~~

# i) Convert BGR and RGB to HSV and GRAY

import cv2
house_color_image = cv2.imread('img.jpeg')
cv2.imshow('Original image',house_color_image)
#BGR 2 HSV
hsv_image = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv_image)
#RGB 2 HSV
hsv_image1 = cv2.cvtColor(house_color_image, cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv_image1)
# BGR 2 GRAY
gray_image = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray_image)
# RGB 2 GRAY
gray_image1 = cv2.cvtColor(house_color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray_image1)

cv2.waitKey(0)
cv2.destroyAllWindows()



# ii)Convert HSV to RGB and BGR

import cv2
sun_color_image = cv2.imread('img.jpeg')
cv2.imshow('Original image', sun_color_image)
hsv_image = cv2.cvtColor(sun_color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' ,hsv_image )
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()




# iii)Convert RGB and BGR to YCrCb

import cv2
sun_color_image = cv2.imread('img.jpeg')
cv2.imshow('Original image', sun_color_image)
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb', gray_image1)
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

# iv)Split and Merge RGB Image

import cv2
image = cv2.imread('img.jpeg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()


# v) Split and merge HSV Image

import cv2
image = cv2.imread('img.jpeg')
hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('H',h)
cv2.imshow('S',s)
cv2.imshow('V',v)
Merged_HSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()


```
## Output:
### i) BGR and RGB to HSV and GRAY
![img1](https://user-images.githubusercontent.com/94881918/228266772-94c08b00-f733-4e65-8056-dcc9093985a4.png)

### ii) HSV to RGB and BGR
![img2](https://user-images.githubusercontent.com/94881918/228267093-a0e059f7-ff76-4987-8252-055bcbc7e2e5.png)


### iii) RGB and BGR to YCrCb
![img3](https://user-images.githubusercontent.com/94881918/228267368-19cd8e61-4586-415d-b632-3b9fde65e722.png)


### iv) Split and merge RGB Image
![img4](https://user-images.githubusercontent.com/94881918/228267434-1a92a7f5-86db-45b7-8130-71b7d53a62b5.png)


### v) Split and merge HSV Image

![img5](https://user-images.githubusercontent.com/94881918/228267481-25e5b91d-50c9-4bbe-a992-b6c248b3b9dc.png)

## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.





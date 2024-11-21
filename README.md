
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.


##### Program:
### Developed By: NAVEEN RAJA N R
### Register Number: 212222230093
### i)Read and Display an Image
Load an image from your local directory and display it
```
import cv2 
image=cv2.imread('car.jpeg',1)
cv2.imshow('WINDOW',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![1](https://github.com/user-attachments/assets/73ed98fb-de7d-47f9-8cc4-4abdb96037b2)


### ii)Draw Shapes and Add Text
(1) Draw a line from the top-left to the bottom-right of the image.
```
import cv2
image = cv2.imread("car.jpeg")
res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (255,0,0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![2](https://github.com/user-attachments/assets/8573e2c8-3c41-4695-8e08-badf77a9d8fe)

(2) Draw a circle at the center of the image.
```
image2=image_resized.copy()
res1=cv2.circle(image2,(250,225),150,(240,0,0),10)
cv2.imshow('Image Window', res1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![3](https://github.com/user-attachments/assets/06066e61-d62f-4d1c-9481-374cc821c027)

(3) Draw a rectangle around a specific region of interest in the image.
```
import cv2

image = cv2.imread("car.jpeg")

height, width = image.shape[:2]


start = (0, 0)
stop = (width - 1, height - 1)

color = (255, 255, 100)
thickness = 10

res_img = cv2.rectangle(image, start, stop, color, thickness)
cv2.imshow('WINDOW', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/6c12d82d-71cd-4d3f-8b3d-447bb3e9f5d1)

(4) Add the text "OpenCV Drawing" at the top-left corner of the image.
```
import cv2
image = cv2.imread("car.jpeg")
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:

![5](https://github.com/user-attachments/assets/70a25f4b-3025-45a9-bb5e-c83b1368380d)


### iii)Image Color Conversion

(1) Convert the image from RGB to HSV and display it
```
import cv2
image = cv2.imread('car.jpeg',1)
cv2.imshow('ORIGINAL IMAGE',image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![6](https://github.com/user-attachments/assets/3196d89f-d3d1-4713-9591-abe36b4a2250)

(2) Convert the image from RGB to GRAY and display it.
```
import cv2
image = cv2.imread('car.jpeg',1)
cv2.imshow('ORIGINAL IMAGE',image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:

![7](https://github.com/user-attachments/assets/8a03ebc2-b849-4dd6-8ac2-6bb65fbc4042)

(3) Convert the image from RGB to YCrCb and display it.
```
import cv2
image = cv2.imread('car.jpeg',1)
cv2.imshow('ORIGINAL IMAGE',image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![8](https://github.com/user-attachments/assets/ede85b93-c2b0-4e17-9a5c-c9c8b1161476)

(4) Convert the HSV image back to RGB and display it.
```
import cv2
image = cv2.imread('car.jpeg',1)
cv2.imshow('ORIGINAL IMAGE',image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![9](https://github.com/user-attachments/assets/163029c0-484c-439e-8c33-bb35c34f9069)

### iv)Access and Manipulate Image Pixels

(1) Access and print the value of the pixel at coordinates (100, 100)
```
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/b4ec5ca1-daff-404f-8054-9990c74051ec)

(2) Modify the color of the pixel at (200, 200) to white
```
import cv2
image = cv2.imread('car.jpeg',1)
cv2.imshow('ORIGINAL IMAGE',image)
image[200, 200] = [255, 255, 255] 
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![11](https://github.com/user-attachments/assets/d13e88b8-74ec-49c8-b10c-96d1ae16813d)

### v)Image Resizing
Resize the original image to half its size and display it.
```
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![12](https://github.com/user-attachments/assets/4ad7049b-3c9a-41c1-9210-e29d4a5a0de0)



### vi)Image Cropping

Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
import cv2
image = cv2.imread('car.jpeg',1)
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![13](https://github.com/user-attachments/assets/d15ce132-acf3-4e6d-83c3-8241570300a2)

### vii)Image Flipping
(1) Flip the original image horizontally and display it.
```
import cv2
image = cv2.imread("car.jpeg")
res=cv2.rotate(image,cv2.ROTATE_180)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

![14](https://github.com/user-attachments/assets/0eb35fd6-89de-4d55-ac40-2dec24812aa6)

(2) Flip the original image vertically and display it.
```
import cv2
image = cv2.imread("car.jpeg")
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:

![15](https://github.com/user-attachments/assets/663edc93-c867-4d48-80eb-f36919f54d10)

### viii)Write and Save the Modified Image

Save the final modified image to your local directory.

```
import cv2
img = cv2.imread("car.jpeg")
cv2.imwrite('boat_pic.jpg',img)
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/4c808c4b-ee3e-4f38-b5fa-f061135bff3c)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







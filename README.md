# Image-Transformation
## AIM
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## ALGORITHM:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image using

M=np.float32([[1,0,20],[0,1,50],[0,0,1]])

translated_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step3:
Scale the image using

M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]])

scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step4:
Shear the image using

M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]])

sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

### Step5:
Reflection of image can be achieved through the code

M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])

reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

### Step6:
Rotate the image using

angle=np.radians(45)

M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])

rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step 7:
Crop the image using

cropped_img=input_img[20:150,60:230]

### Step 8:
Display all the Transformed images.

## Program:
```python
Developed By: J . RITHANIEPRIYANKA
Register Number: 212220230039
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("img.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape

i)Image Translation

M=np.float32([[1,0,20],
             [0,1,50],
             [0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()

ii) Image Scaling
M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()

iii)Image shearing
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.4,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()

iv)Image Reflection
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()

v)Image Rotation
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()

vi)Image Cropping
cropped_img=input_img[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation

![EXP5-A](https://user-images.githubusercontent.com/75235132/165502967-1af3d4cd-5c20-4cdb-a04d-2a460a364d5c.png)

### ii) Image Scaling

![EXP5-B](https://user-images.githubusercontent.com/75235132/165502986-8d9d43e5-f28e-4f60-b146-faace33b6fe4.png)

### iii)Image shearing

![EXP5-C](https://user-images.githubusercontent.com/75235132/165503009-430cdbe8-50d8-4c5a-ba0a-9beab151676e.png)

### iv)Image Reflection

![EXP5-D](https://user-images.githubusercontent.com/75235132/165503018-d06e9a79-0352-4fbd-9c33-f1c140819034.png)

### v)Image Rotation

![EXP5-E](https://user-images.githubusercontent.com/75235132/165503035-9bafa408-ba1d-40ea-8843-5c754cc491cb.png)

### vi)Image Cropping

![EXP5-F](https://user-images.githubusercontent.com/75235132/165503060-c5f99f82-886f-4da3-9d3a-3ce46ffdd011.png)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.

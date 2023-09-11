# EXP-5 IMAGE TRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image.

### Step3:
Scale the image.

### Step4:
Shear the image.

### Step5:
Find reflection of image.

### Step6:
Rotate the image.

### Step7:
Crop the image.

### Step8:
Display all the Transformed images.

## Program:
```
Developed By: SASIDEVI V
Register Number: 212222230136
```
```
i)Image Translation

import numpy as np
import cv2
import matplotlib.pyplot as plt
image=cv2.imread("tune.jpg")
image=cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(image)
plt.show()
rows,cols,dim=image.shape
M=np.float32([[1,0,100],[0,1,200],[0,0,1]])
translated_image=cv2.warpPerspective(image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()


ii) Image Scaling

rows,cols,dim=image.shape
M=np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
scaled_img=cv2.warpPerspective(image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()


iii)Image shearing

rows,cols,dim = image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()


iv)Image Reflection

rows,cols,dim = image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(image,M_Y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()


v)Image Rotation

rows,cols,dim = image.shape
angle = np.radians(30)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()


vi)Image Cropping

rows,cols,dim = image.shape
cropped_img=image[11:500,27:630]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()

```
## Output:
### INPUT IMAGE

![image](https://github.com/SASIDEVIvenaram/IMAGETRANSFORMATION/assets/118707332/820307f6-6fb8-47fa-92a0-86bc59476a53)

### i)Image Translation

![image](https://github.com/SASIDEVIvenaram/IMAGETRANSFORMATION/assets/118707332/f0807c8f-5051-4956-ae0c-b7fbe1812118)
### ii) Image Scaling

![image](https://github.com/SASIDEVIvenaram/IMAGETRANSFORMATION/assets/118707332/49914dc9-d93d-478a-93b0-e305c3537308)



### iii)Image shearing

![image](https://github.com/SASIDEVIvenaram/IMAGETRANSFORMATION/assets/118707332/aff4088e-0df6-46e6-9fd1-ec268c83e070)
![image](https://github.com/SASIDEVIvenaram/IMAGETRANSFORMATION/assets/118707332/0af76a10-9325-41aa-9944-2a4421fa7c2f)




### iv)Image Reflection
![image](https://github.com/SASIDEVIvenaram/IMAGETRANSFORMATION/assets/118707332/14f40ecc-7529-4be5-8db7-342460374209)
![image](https://github.com/SASIDEVIvenaram/IMAGETRANSFORMATION/assets/118707332/bc4b339c-4717-4467-b4aa-bb0dc560e667)


### v)Image Rotation
![image](https://github.com/SASIDEVIvenaram/IMAGETRANSFORMATION/assets/118707332/4304abfa-bb48-4190-969d-7f6a333fefe7)



### vi)Image Cropping
![image](https://github.com/SASIDEVIvenaram/IMAGETRANSFORMATION/assets/118707332/143ce0dc-ee27-4087-9017-8face9d343b1)





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.

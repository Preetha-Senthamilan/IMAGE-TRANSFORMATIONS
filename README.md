## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image using a function warpPerpective()

### Step3:
Scale the image by multiplying the rows and columns with a float value

### Step4:
Shear the image in both the rows and columns.

### Step5:
Find the reflection of the image.

### Step 6:
Rotate the image using angle function.

## Program:
```
Developed By:PREETHA.S
Register Number:212222230110

i)Image Translation
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("pre.jpeg")
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,50],  [0,1,100],  [0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()

ii) Image Scaling
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("pre.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()


iii)Image shearing
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("pre.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()


iv)Image Reflection
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("pre.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()


v)Image Rotation
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("pre.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()


vi)Image Cropping
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("pre.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()

```
## Output:
### i)Image Translation

![image](https://github.com/Preetha-Senthamilan/IMAGE-TRANSFORMATIONS/assets/119390282/7f8f2dab-cdc5-46a5-9065-8d6baf1f2254)


![image](https://github.com/Preetha-Senthamilan/IMAGE-TRANSFORMATIONS/assets/119390282/37ef9a90-bfac-47ad-a68a-5210ddd1133b)



### ii) Image Scaling

![image](https://github.com/Preetha-Senthamilan/IMAGE-TRANSFORMATIONS/assets/119390282/71dddee2-f501-473a-897b-aa1c099bf9b9)

![image](https://github.com/Preetha-Senthamilan/IMAGE-TRANSFORMATIONS/assets/119390282/1c5198b0-da0e-41a5-9f62-4730ad2def3b)


### iii)Image shearing

![image](https://github.com/Preetha-Senthamilan/IMAGE-TRANSFORMATIONS/assets/119390282/07d4aac0-c9f1-4452-9468-e8984344ff5b)

![image](https://github.com/Preetha-Senthamilan/IMAGE-TRANSFORMATIONS/assets/119390282/3affd6da-fedd-4db4-bd7c-82c0bb52a483)

![image](https://github.com/Preetha-Senthamilan/IMAGE-TRANSFORMATIONS/assets/119390282/c7b5b7e7-3e02-4ed8-858e-857402ef0737)



### iv)Image Reflection

![image](https://github.com/Preetha-Senthamilan/IMAGE-TRANSFORMATIONS/assets/119390282/91152865-cd28-490c-81b7-09fcd4938689)

![image](https://github.com/Preetha-Senthamilan/IMAGE-TRANSFORMATIONS/assets/119390282/2fc5ce3d-d5fa-4276-ac12-5278a79f2ae6)

![image](https://github.com/Preetha-Senthamilan/IMAGE-TRANSFORMATIONS/assets/119390282/fea75e4e-d402-4542-9a24-05a7a122e440)



### v)Image Rotation

![image](https://github.com/Preetha-Senthamilan/IMAGE-TRANSFORMATIONS/assets/119390282/37d84e9c-5dab-44d3-88f1-15e66181bdc6)

![image](https://github.com/Preetha-Senthamilan/IMAGE-TRANSFORMATIONS/assets/119390282/328f362d-9ad3-4425-9d7b-483f36d09ae8)

![image](https://github.com/Preetha-Senthamilan/IMAGE-TRANSFORMATIONS/assets/119390282/19ab469a-30fc-4550-8708-7fb2ada1b817)


### vi)Image Cropping

![image](https://github.com/Preetha-Senthamilan/IMAGE-TRANSFORMATIONS/assets/119390282/224b6bac-901c-4a0c-9557-d6ba4e24a741)

![image](https://github.com/Preetha-Senthamilan/IMAGE-TRANSFORMATIONS/assets/119390282/d9cfb3d9-52f6-4ec3-97d7-cb45ff3bd76f)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.

# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the image using imread()

### Step2:
print the image using imshow()
### Step3:
import numpy for take the pixels in matrix form
### Step4:
import matplotlib.pyplot for showing the image.
### Step5:
By importing the open cv we can change image color.
## Program:
```python
Developed By:Arikatla Hari Veera Prasad
Register Number:212223240014
i)Image Translation
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('bookcover.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,100],[0,1,200],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()

ii) Image Scaling
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('bookcover.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(translated_image)
plt.show()


iii)Image shearing
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('bookcover.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M2=np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols*1.5),int(rows*1.5)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()


iv)Image Reflection
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('bookcover.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M2=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols),int(rows)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()



v)Image Rotation
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('bookcover.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(translated_image)
plt.show()



vi)Image Cropping

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('bookcover.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(translated_image)
plt.show()



```
## Output:
### i)Image Translation
![image](https://github.com/Hariveeraprasad-2006/IMAGE-TRANSFORMATIONS/assets/145049988/498a3b6f-3947-4560-947d-eeaad9c490e4)
### ii) Image Scaling
![image](https://github.com/Hariveeraprasad-2006/IMAGE-TRANSFORMATIONS/assets/145049988/97a55f96-2f84-43cf-8646-32a7624598c9)
### iii)Image shearing
![image](https://github.com/Hariveeraprasad-2006/IMAGE-TRANSFORMATIONS/assets/145049988/19837959-5ea0-492d-97c7-de416383be44)
### iv)Image Reflection
![image](https://github.com/Hariveeraprasad-2006/IMAGE-TRANSFORMATIONS/assets/145049988/d1cb678e-ec8e-4113-9987-c4d84714990b)
### v)Image Rotation
![image](https://github.com/Hariveeraprasad-2006/IMAGE-TRANSFORMATIONS/assets/145049988/9b025ec0-fb44-4ab2-a53a-2f4bcd32db86)
### vi)Image Cropping
![image](https://github.com/Hariveeraprasad-2006/IMAGE-TRANSFORMATIONS/assets/145049988/071dcd3e-68da-4215-ab10-ee72dbafb13c)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.

# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
<br>Translate the image using a function warpPerpective()

### Step3:
<br>Scale the image by multiplying the rows and columns with a float value.

### Step4:
<br>Shear the image in both the rows and columns.

### Step5:
<br>Find the reflection of the image.

### Step6:
<br>Rotate the image using angle function.

## Program:
```python
Developed By: PRAGAHARSHITHA NC
Register Number: 212222110033
```

i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("book.jpeg")
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
```


ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("obj.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```


iii)Image shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("obj.jpeg")
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
```


iv)Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("obj.jpeg")
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
```



v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("obj.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()

angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(input_image,M,(int(cols),int(rows)))

plt.imshow(rotated_img)
plt.show()
```



vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("obj.jpeg")
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
![image](https://github.com/JoyceBeulah/IMAGE-TRANSFORMATIONS/assets/118343698/d37be835-521f-43cd-a51c-2e110234ff84)

### ii) Image Scaling
![image](https://github.com/JoyceBeulah/IMAGE-TRANSFORMATIONS/assets/118343698/b293443f-ed9f-47c8-aa91-98ffb6c1a828)

### iii)Image shearing
![image](https://github.com/JoyceBeulah/IMAGE-TRANSFORMATIONS/assets/118343698/889b24b3-722b-4249-a267-1de6303d2203)

### iv)Image Reflection
![image](https://github.com/JoyceBeulah/IMAGE-TRANSFORMATIONS/assets/118343698/a3ad8e8b-4b89-4558-8558-e19b21a72155)

### v)Image Rotation
![image](https://github.com/JoyceBeulah/IMAGE-TRANSFORMATIONS/assets/118343698/ad569f81-20c4-442d-acac-dd125aa8ab96)

### vi)Image Cropping
![image](https://github.com/JoyceBeulah/IMAGE-TRANSFORMATIONS/assets/118343698/116d8a88-563d-4f24-a343-f36ba57cfe42)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.

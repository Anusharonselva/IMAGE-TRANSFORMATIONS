# IMAGE-TRANSFORMATIONS


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
Developed By:S.ANUSHARON
Register Number:212222240010
i)Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image = cv2.warpPerspective(lion_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
ii) Image Scaling
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
scaled_img = cv2.warpPerspective(lion_image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```



iii)Image shearing
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(lion_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(lion_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()
```



iv)Image Reflection
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
dog_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(lion_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(lion_image,M_Y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()
```




v)Image Rotation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
angle = np.radians(30)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(lion_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```



vi)Image Cropping
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
cropped_img=lion_image[11:500,27:630]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```





## Output:
### i)Image Translation
![Screenshot 2024-03-19 111312](https://github.com/Anusharonselva/IMAGE-TRANSFORMATIONS/assets/119405600/7a0412df-023e-4d51-b033-fdc4806a547d)

![Screenshot 2024-03-19 111327](https://github.com/Anusharonselva/IMAGE-TRANSFORMATIONS/assets/119405600/1745d910-5fd8-4247-a84c-0c64ede6ecab)


### ii) Image Scaling
![Screenshot 2024-03-19 111924](https://github.com/Anusharonselva/IMAGE-TRANSFORMATIONS/assets/119405600/82c4508f-af0c-496f-b86e-a0e0379c470b)

![Screenshot 2024-03-19 111937](https://github.com/Anusharonselva/IMAGE-TRANSFORMATIONS/assets/119405600/12b4ee68-bd38-4fcd-b5ca-5298e4c32b7d)


### iii)Image shearing
![Screenshot 2024-03-19 112038](https://github.com/Anusharonselva/IMAGE-TRANSFORMATIONS/assets/119405600/d14b4eb1-6869-4910-a89f-46f081d3cea1)
![Screenshot 2024-03-19 112049](https://github.com/Anusharonselva/IMAGE-TRANSFORMATIONS/assets/119405600/198458b4-0ea8-459c-86e8-8d61d32b73ae)
![Screenshot 2024-03-19 112101](https://github.com/Anusharonselva/IMAGE-TRANSFORMATIONS/assets/119405600/677b412d-d7e4-4b28-ab1b-f7709f9e3a25)



### iv)Image Reflection
![Screenshot 2024-03-19 112144](https://github.com/Anusharonselva/IMAGE-TRANSFORMATIONS/assets/119405600/f5a05d78-c103-4c13-96dc-bf6d73d2239c)
![Screenshot 2024-03-19 112156](https://github.com/Anusharonselva/IMAGE-TRANSFORMATIONS/assets/119405600/117b07ed-878e-47bc-a015-7cf731f5f3be)

![Screenshot 2024-03-19 112208](https://github.com/Anusharonselva/IMAGE-TRANSFORMATIONS/assets/119405600/ee799309-8181-44a2-977f-73973be1fe60)



### v)Image Rotation
![Screenshot 2024-03-19 112240](https://github.com/Anusharonselva/IMAGE-TRANSFORMATIONS/assets/119405600/1a351889-db80-4e66-91d1-4c2575dbe415)

![Screenshot 2024-03-19 112250](https://github.com/Anusharonselva/IMAGE-TRANSFORMATIONS/assets/119405600/97c8f26b-dc7b-4182-b88f-5262d1f72f4a)



### vi)Image Cropping

![Screenshot 2024-03-19 112351](https://github.com/Anusharonselva/IMAGE-TRANSFORMATIONS/assets/119405600/1564d562-c5a3-4d10-b968-386fbc34fa07)

![Screenshot 2024-03-19 112401](https://github.com/Anusharonselva/IMAGE-TRANSFORMATIONS/assets/119405600/1873b786-f679-408c-94ed-19f2fa36b04b)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.

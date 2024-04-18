## Implementation-of-Erosion-and-Dilation
### Aim
To implement Erosion and Dilation using Python and OpenCV.
### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:<br>
Import the necessary pacakages

#### Step2:<br>
Create the text using cv2.putText

#### Step3:<br>
Create the structuring element

#### Step4:<br>
Erode the image


#### Step5: <br>
Dilate the Image

 
### Program:
Developed by: YUVASAKTHI N.C
Register Number:212222240120

##### Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
##### Create the Text using cv2.putText
``` Python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'Lifestyle',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
##### Create the structuring element
``` Python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
##### Erode the image
``` Python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

```
##### Dilate the image
``` Python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')



```
### Output:

#### Display the input Image
![image](https://github.com/IamShakthi/erosion--dilation/assets/117913445/dd9a9f3e-39e4-49ad-b36a-a24ac567686d)


#### Display the Eroded Image

![image](https://github.com/IamShakthi/erosion--dilation/assets/117913445/5cefd8f5-128c-4fe5-83b4-444cd3f3884b)



#### Display the Dilated Image

![image](https://github.com/IamShakthi/erosion--dilation/assets/117913445/7b732983-e9ac-45bd-a710-3428bf9c659c)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.

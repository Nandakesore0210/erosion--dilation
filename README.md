# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

 
## Program:

```
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline

def load_img():
    blank_img =np.zeros((600,600))
    font = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_img,text='NANDU',org=(50,300), fontFace=font,fontScale= 5,color=(255,255,255),thickness=25,lineType=cv2.LINE_AA)
    return blank_img

def display_img(img):
    fig = plt.figure(figsize=(12,10))
    ax = fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    plt.show()

img = load_img()
display_img(img)

# Erode the image
kernel = np.ones((5,5),dtype=np.uint8)
erosion1 = cv2.erode(img,kernel,iterations = 1)
display_img(erosion1)

# Dilate the image
img = load_img()
kernel = np.ones((5,5),np.uint8)
erosion5 = cv2.erode(img,kernel,iterations = 4)
display_img(erosion5)

```
## Output:

### Display the input Image
![image](https://github.com/user-attachments/assets/47b7a683-5f77-4b5f-aa61-d8cdf2964141)

### Display the Eroded Image
![image](https://github.com/user-attachments/assets/42a06f02-5f20-4246-9cf9-f1142d520bc4)

### Display the Dilated Image
![image](https://github.com/user-attachments/assets/7aa5311f-a407-424b-bb37-92ec305e0295)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.

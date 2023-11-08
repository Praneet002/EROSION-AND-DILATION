# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import necessary packages

### Step2:
Create an empty window and add text to it
### Step3:
create a structuring element

### Step4:
Do the operation

### Step5:
Show the output image

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np


# Create the Text using cv2.putText

IMg= np.zeros((350,1400),dtype ='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,'Praneet',(15,200),font,5,(255),10,cv2.LINE_AA)
cv2.imshow('created_text',img)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element



# Erode the image

erode1= np.ones((5,5),np.uint8)
erode2 = cv2.getStructuringElement(cv2.MORPH_CROSS,(12,12))

image_erode1 = cv2.erode(img,erode1)
cv2.imshow('Eroded_image_1',image_erode1)
cv2.waitKey(0)
cv2.destroyAllWindows()
image_erode2 = cv2.erode(img,erode2)
cv2.imshow('Eroded_image_2',image_erode2)
cv2.waitKey(0)
cv2.destroyAllWindows()


# Dilate the image


dilate1= np.ones((5,5),np.uint8)
dilate2 = cv2.getStructuringElement(cv2.MORPH_CROSS,(12,12))

image_dilate1 = cv2.dilate(img,dilate1)
cv2.imshow('Dilated_image_1',image_dilate1)
cv2.waitKey(0)
cv2.destroyAllWindows()
image_dilated2 = cv2.dilate(img,dilate2)
cv2.imshow('Dilated_image_2',image_dilated2)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:

### Display the input Image
![Screenshot 2023-11-08 085809](https://github.com/Praneet002/EROSION-AND-DILATION/assets/94308200/e250b046-0ba0-45cd-9093-b735b09a9889)



### Display the Eroded Image
![Screenshot 2023-11-08 085821](https://github.com/Praneet002/EROSION-AND-DILATION/assets/94308200/b94c6f94-9b84-4888-b029-b8073bf63f4c)
![Screenshot 2023-11-08 085832](https://github.com/Praneet002/EROSION-AND-DILATION/assets/94308200/a8e1b0ea-0d3e-4247-bb71-47d765909e7c)


### Display the Dilated Image

![Screenshot 2023-11-08 085842](https://github.com/Praneet002/EROSION-AND-DILATION/assets/94308200/08dde27b-a177-4338-a4ad-30ae34cebbb5)
![Screenshot 2023-11-08 085853](https://github.com/Praneet002/EROSION-AND-DILATION/assets/94308200/e2ae1d75-950f-4648-9ff6-e46140f46ba8)


## Result
Thus the generated text image is eroded and dilated using Python and OpenCV.

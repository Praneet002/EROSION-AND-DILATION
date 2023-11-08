# EROSION-AND-DILATION

Implementation-of-Erosion-and-Dilation
# Aim
To implement Erosion and Dilation using Python and OpenCV.
# Software Required
1. Anaconda - Python 3.7
2. OpenCV
# Algorithm:
Step1:
Import necessary packages
Step2:
Create an empty window and add text to it
Step3:
create a structuring element
Step4:
Do the operation
Step5:
Show the output image

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np



# Create the Text using cv2.putText
img= np.zeros((350,1400),dtype ='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,'Praneet',(15,200),font,5,(255),10,cv2.LINE_AA)
cv2.imshow('created_text',img)
cv2.waitKey(0)
cv2.destroyAllWindows()



# Create the structuring element
# For Erosion
erode1= np.ones((5,5),np.uint8)
erode2 = cv2.getStructuringElement(cv2.MORPH_CROSS,(12,12))



# Erode the image
# For Dilation
dilate1= np.ones((5,5),np.uint8)
dilate2 = cv2.getStructuringElement(cv2.MORPH_CROSS,(12,12))

# Erode and show the eroded image
image_erode1 = cv2.erode(img,erode1)
cv2.imshow('Eroded_image_1',image_erode1)
cv2.waitKey(0)
cv2.destroyAllWindows()
image_erode2 = cv2.erode(img,erode2)
cv2.imshow('Eroded_image_2',image_erode2)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Dilate and show dilated the image
image_dilate1 = cv2.dilate(img,dilate1)
cv2.imshow('Dilated_image_1',image_dilate1)
cv2.waitKey(0)
cv2.destroyAllWindows()
212221230042
55
image_dilated2 = cv2.dilate(img,dilate2)
cv2.imshow('Dilated_image_2',image_dilated2)
cv2.waitKey(0)
cv2.destroyAllWindows()






```
## Output:

### Display the input Image
<br>
<br>![Screenshot 2023-11-08 085809](https://github.com/Praneet002/EROSION-AND-DILATION/assets/94308200/abcb20aa-8bb7-4185-81e5-90a8a897f838)


<br>
<br>
<br>
<br>

### Display the Eroded Image
<br>
<br>![Screenshot 2023-11-08 085821](https://github.com/Praneet002/EROSION-AND-DILATION/assets/94308200/3451883f-4678-4b14-9738-25e1450f95b3)


<br>
<br>![Screenshot 2023-11-08 085832](https://github.com/Praneet002/EROSION-AND-DILATION/assets/94308200/9cc725c0-5903-4e32-b137-8b2171a24a8d)


<br>
<br>

### Display the Dilated Image
<br>
<br>![Screenshot 2023-11-08 085842](https://github.com/Praneet002/EROSION-AND-DILATION/assets/94308200/24806098-d792-4a2e-a7b2-7a9f70deb7f9)


<br>
<br>![Screenshot 2023-11-08 085853](https://github.com/Praneet002/EROSION-AND-DILATION/assets/94308200/40070217-7b1f-48cf-98c4-c0f02c75a902)


<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.

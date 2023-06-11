Exp.No : 10 
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
Date : 10.05.2023 
<br>
# Implementation of Erosion and Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
- **Step1:** Import the necessary packages.
- **Step2:** Create the text image using cv2.putText().
- **Step3:** Create the structuring kernel for image dilation and erosion.
- **Step4:** Apply erosion and dilation using cv2.erode and cv2.dilate.
- **Step5:** Plot the images using plt.imshow().

## Program:
> program by : Kaushika A <br>
> reg no : 212221230048

**Import the necessary packages**
``` Python
import cv2
import numpy as np
from matplotlib import pyplot as plt
```
**Create the Text using cv2.putText**
```python
# Create the text using cv2.putText
text_image = np.zeros((100,250),dtype = 'uint8')
font = cv2.FONT_HERSHEY_COMPLEX_SMALL
cv2.putText(text_image,"Kaushika",(5,70),font,2,(255),2,cv2.LINE_AA) 
plt.title("Original Image")
plt.imshow(text_image,'Blues')
plt.axis('off')
```
**Create the structuring element**
```python
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(4,4))
```
**Erode and Dilate the image**
```python
image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'Blues')
plt.axis('off')

image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'Blues')
plt.axis('off')
```
## Output:

**Display the input Image**

<img src="https://github.com/Kaushika-Anandh/Implementation-of-Erosion-and-Dilation/blob/main/1.png" width="310" height="140">

**Display the Eroded Image**

<img src="https://github.com/Kaushika-Anandh/Implementation-of-Erosion-and-Dilation/blob/main/2.png" width="310" height="140">

**Dilated Image**

<img src="https://github.com/Kaushika-Anandh/Implementation-of-Erosion-and-Dilation/blob/main/3.png" width="310" height="140">

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.

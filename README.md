# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:

```
NAME: CH.V.SIVA DINESH KUMAR
REG NO: 212224040055
```
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```
# Load the color image
image = cv2.imread(''/content/puppy.jpg')
```
```
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```
```
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
<img width="513" height="411" alt="download" src="https://github.com/user-attachments/assets/5ecbbd37-bc31-4234-8449-0595b5e9ca9f" />

```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
```
```
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
```
<img width="513" height="411" alt="download" src="https://github.com/user-attachments/assets/9a71b593-5d28-48ee-a098-596737044a99" />

```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
```
```
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
<img width="553" height="435" alt="download" src="https://github.com/user-attachments/assets/0dbc43ae-84d3-4b9e-9d1b-db4174bcb920" />

```
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
```
```
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.show()
```
<img width="552" height="435" alt="download" src="https://github.com/user-attachments/assets/0c6f6375-b5e9-4355-ae46-46ca63a1cb36" />


### Histogram for Daerk Image 
```
import cv2
import numpy as np
from matplotlib import pyplot as plt
```
```
# Load the color image
image = cv2.imread('dog.jpg')
```
```
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```
```
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
<img width="515" height="373" alt="download" src="https://github.com/user-attachments/assets/b207e1f7-6e50-4bd4-935f-f033f3568617" />


```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
```
```
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
```
<img width="515" height="373" alt="download" src="https://github.com/user-attachments/assets/1a13646e-d1db-43e5-b5bd-c3b51b65e321" />



```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
```
```

plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

```
<img width="562" height="435" alt="download" src="https://github.com/user-attachments/assets/8e6819e9-4bdc-4bd9-a75b-e119d235b2f4" />


```
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
```
```
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.show()
```

<img width="560" height="435" alt="download" src="https://github.com/user-attachments/assets/48f8be21-626d-49bc-b19e-cda2e599d567" />





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.


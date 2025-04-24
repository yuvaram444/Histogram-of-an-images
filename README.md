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
``` python
# Developed By: YUVARAM . S
# Register Number: 212224230315
```
### Input Grayscale Image and Color Image:
```
import cv2
from matplotlib import pyplot as plt
# Load the color image
image = cv2.imread("C:/Users/admin/OneDrive/Pictures/peacock.png")
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
### Histogram of Grayscale Image and any channel of Color Image
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
### Apply histogram equalization
```
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
```
### Histogram Equalization of Grayscale Image.
```
hist_original = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2025-04-24 081424](https://github.com/user-attachments/assets/781af84a-eab0-4756-8ce8-43813ee733ce)


### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2025-04-24 081437](https://github.com/user-attachments/assets/01e98dad-7cb1-4f40-b695-ffc2d3370545)


### Apply histogram equalization
![Screenshot 2025-04-24 081450](https://github.com/user-attachments/assets/e5dd849c-3d7b-4457-a5ef-09b0066591e4)

### Histogram Equalization of Grayscale Image.

![Screenshot 2025-04-24 081506](https://github.com/user-attachments/assets/c059b443-eb74-46f5-aa89-bd2bc2f32d87)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.

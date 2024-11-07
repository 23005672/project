# Project
## Aim
To write a python program using OpenCV to do the following image manipulations.
i) Extract ROI from  an image.
ii) Perform handwritting detection in an image.
iii) Perform object detection with label in an image.
## Software Required:
Anaconda - Python 3.7
## Algorithm:
## I)Perform ROI from an image
### Step1:
Import necessary packages 
### Step2:
Read the image and convert the image into RGB
### Step3:
Display the image
### Step4:
Set the pixels to display the ROI 
### Step5:
Perform bit wise conjunction of the two arrays  using bitwise_and 
### Step6:
Display the segmented ROI from an image.

## Program:
```
Name   : RIYA P L
Reg no : 212223240141
```
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 1: Read and convert the image to RGB format
image = cv2.imread('image.jpg')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

# Step 2: Display the original image
plt.imshow(image_rgb)
plt.title('Original Image')
plt.axis('off')

# Step 3: Create an ROI mask
roi_mask = np.zeros_like(image_rgb)
roi_mask[100:250, 100:250, :] = 255  # Define the ROI region(Dog-face)

# Step 4: Segment the ROI using bitwise AND operation
segmented_roi = cv2.bitwise_and(image_rgb, roi_mask)

# Step 5: Display the segmented ROI
plt.imshow(segmented_roi)
plt.title('Region of Interest')
plt.axis('off')

# Show both images side by side
plt.show()
```

## Output:

![Screenshot 2024-11-07 222628](https://github.com/user-attachments/assets/db035452-2928-4a96-8276-f9dd59c125ad)

![Screenshot 2024-11-07 222651](https://github.com/user-attachments/assets/becc1f52-526c-48e1-bf17-35f4862ae019)

## II)Perform handwritting detection in an image
### Step1:
Import necessary packages 
### Step2:
Define a function to read the image,Convert the image to grayscale,Apply Gaussian blur to reduce noise and improve edge detection,Use Canny edge detector to find edges in the image,Find contours in the edged image,Filter contours based on area to keep only potential text regions,Draw bounding boxes around potential text regions.
### Step3:
Display the results.

## Output:

![Screenshot 2024-11-07 222711](https://github.com/user-attachments/assets/2cfecde1-cc06-4844-bd6d-82c309c3d221)

## III)Perform object detection with label in an image
### Step1:
Import necessary packages 
### Step2:
Set and add the config_file,weights to ur folder.
### Step3:
Use a pretrained Dnn model (MobileNet-SSD v3)
### Step4:
Create a classLabel and print the same
### Step5:
Display the image using imshow()
### Step6:
Set the model and Threshold to 0.5
### Step7:
Flatten the index,confidence.
### Step8:
Display the result.

## Output:

![Screenshot 2024-11-07 222738](https://github.com/user-attachments/assets/678c00a5-e431-481e-8e76-50721cd03fb9)

## Result:

Thus, a python program using OpenCV for following image manipulations are done successfully.


# IMAGE-TRANSFORMATIONS
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>

### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

## Program:
```python
Developed By: JEEVITHA S
Register Number:212222100016

i)Image Translation

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Function to display images in Colab
def show_image(image):
    plt.figure(figsize=(6, 6))
    plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
    plt.axis('off')
    plt.show()

# Load an image from URL or file path
image_url = 'rose.jpg' 
image = cv2.imread(image_url)

# Define translation matrix
tx = 50  # Translation along x-axis
ty = 30  # Translation along y-axis
translation_matrix = np.float32([[1, 0, tx], [0, 1, ty]])  # Create translation matrix

# Apply translation to the image
translated_image = cv2.warpAffine(image, translation_matrix, (image.shape[1], image.shape[0]))

# Display original and translated images
print("Original Image:")
show_image(image)
print("Translated Image:")
show_image(translated_image)


ii) Image Scaling

#Install OpenCV library if not already installed
!pip install opencv-python-headless

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Function to display images in Colab
def show_image(image):
    plt.figure(figsize=(6, 6))
    plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
    plt.axis('off')
    plt.show()

# Load an image from URL or file path
image_url = 'rose.jpg'  # Replace with your image URL or file path
image = cv2.imread(image_url)

# Define scale factors
scale_x = 1.5  # Scaling factor along x-axis
scale_y = 1.5  # Scaling factor along y-axis

# Apply scaling to the image
scaled_image = cv2.resize(image, None, fx=scale_x, fy=scale_y, interpolation=cv2.INTER_LINEAR)

# Display original and scaled images
print("Original image:")
show_image(image)
print("Scaled Image:")
show_image(scaled_image)


iii)Image shearing

# Install OpenCV library if not already installed
!pip install opencv-python-headless

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Function to display images in Colab
def show_image(image):
    plt.figure(figsize=(6, 6))
    plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
    plt.axis('off')
    plt.show()

# Load an image from URL or file path
image_url = 'rose.jpg'  # Replace with your image URL or file path
image = cv2.imread(image_url)

# Define shear parameters
shear_factor_x = 0.5  # Shear factor along x-axis
shear_factor_y = 0.2  # Shear factor along y-axis

# Define shear matrix
shear_matrix = np.float32([[1, shear_factor_x, 0], [shear_factor_y, 1, 0]])

# Apply shear to the image
sheared_image = cv2.warpAffine(image, shear_matrix, (image.shape[1], image.shape[0]))

# Display original and sheared images
print("Original Image:")
show_image(image)
print("Sheared Image:")
show_image(sheared_image)



iv)Image Reflection

# Install OpenCV library if not already installed
!pip install opencv-python-headless

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Function to display images in Colab
def show_image(image):
    plt.figure(figsize=(6, 6))
    plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
    plt.axis('off')
    plt.show()

# Load an image from URL or file path
image_url = 'rose.jpg'  # Replace with your image URL or file path
image = cv2.imread(image_url)

# Reflect the image horizontally
reflected_image_horizontal = cv2.flip(image, 1)

# Reflect the image vertically
reflected_image_vertical = cv2.flip(image, 0)

# Reflect the image both horizontally and vertically
reflected_image_both = cv2.flip(image, -1)

# Display original and reflected images
print("Original Image:")
show_image(image)
print("Reflected Horizontally:")
show_image(reflected_image_horizontal)
print("Reflected Vertically:")
show_image(reflected_image_vertical)
print("Reflected Both:")
show_image(reflected_image_both)




v)Image Rotation


# Install OpenCV library if not already installed
!pip install opencv-python-headless

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Function to display images in Colab
def show_image(image):
    plt.figure(figsize=(6, 6))
    plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
    plt.axis('off')
    plt.show()

# Load an image from URL or file path
image_url = 'rose.jpg'  # Replace with your image URL or file path
image = cv2.imread(image_url)

# Define rotation angle in degrees
angle = 45

# Get image height and width
height, width = image.shape[:2]

# Calculate rotation matrix
rotation_matrix = cv2.getRotationMatrix2D((width / 2, height / 2), angle, 1)

# Perform image rotation
rotated_image = cv2.warpAffine(image, rotation_matrix, (width, height))

# Display original and rotated images
print("Original Image:")
show_image(image)
print("Rotated Image:")
show_image(rotated_image)





vi)Image Cropping

# Install OpenCV library if not already installed
!pip install opencv-python-headless

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Function to display images in Colab
def show_image(image):
    plt.figure(figsize=(6, 6))
    plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
    plt.axis('off')
    plt.show()

# Load an image from URL or file path
image_url = 'rose.jpg'  # Replace with your image URL or file path
image = cv2.imread(image_url)

# Define cropping coordinates (x, y, width, height)
x = 100  # Starting x-coordinate
y = 50   # Starting y-coordinate
width = 200  # Width of the cropped region
height = 150  # Height of the cropped region

# Perform image cropping
cropped_image = image[y:y+height, x:x+width]

# Display original and cropped images
print("Original Image:")
show_image(image)
print("Cropped Image:")
show_image(cropped_image)
```
## Output:
### i)Image Translation
![315514006-1946d4ff-d274-448a-8342-957d981a00d8](https://github.com/Jeevithha/IMAGE-TRANSFORMATIONS/assets/123623197/57c7f74d-f9d0-45a4-ac1a-fc5419dbe34f)
![315514006-1946d4ff-d274-448a-8342-957d981a00d8](https://github.com/Jeevithha/IMAGE-TRANSFORMATIONS/assets/123623197/91cdb35a-8252-4e73-a966-978cfe33d2c4)

### ii) Image Scaling
![315514674-e293be4d-3c54-4a29-866a-dca65583f169](https://github.com/Jeevithha/IMAGE-TRANSFORMATIONS/assets/123623197/9634c435-097b-4d6d-bdbc-502f0f58d685)
![315514674-e293be4d-3c54-4a29-866a-dca65583f169](https://github.com/Jeevithha/IMAGE-TRANSFORMATIONS/assets/123623197/d4e464cd-bf74-43c4-ab71-721f54b85121)

### iii)Image shearing
![315515149-e4b37d2d-cd18-402d-bdfd-5656cef4d2cd](https://github.com/Jeevithha/IMAGE-TRANSFORMATIONS/assets/123623197/13f33c08-a1ed-444b-b146-8efc8f22fd4a)
![315515149-e4b37d2d-cd18-402d-bdfd-5656cef4d2cd](https://github.com/Jeevithha/IMAGE-TRANSFORMATIONS/assets/123623197/79bbae93-d4ff-466c-8161-7fa243f5a65c)

### iv)Image Reflection
![315515874-45bd371d-ca49-4344-ae58-f9273c7979d4](https://github.com/Jeevithha/IMAGE-TRANSFORMATIONS/assets/123623197/996de018-9748-459a-90da-c5c76794bdcb)
![315515874-45bd371d-ca49-4344-ae58-f9273c7979d4](https://github.com/Jeevithha/IMAGE-TRANSFORMATIONS/assets/123623197/fd7a8fa0-8837-41cd-92c6-f3f72a684266)
![315516184-928d7451-7600-4f9e-ac8d-53170438e2fd](https://github.com/Jeevithha/IMAGE-TRANSFORMATIONS/assets/123623197/ea38d768-e489-40b7-8546-dc3d7506a789)
![315516184-928d7451-7600-4f9e-ac8d-53170438e2fd](https://github.com/Jeevithha/IMAGE-TRANSFORMATIONS/assets/123623197/3b705008-84f1-46ca-8541-3b5ec3492b9f)
### v)Image Rotation
![315516663-5e8f5771-f4e9-4b9c-93b7-d1487f0a1702](https://github.com/Jeevithha/IMAGE-TRANSFORMATIONS/assets/123623197/1a696ea6-a3ec-4819-8af7-82c28a113894)
![315516663-5e8f5771-f4e9-4b9c-93b7-d1487f0a1702](https://github.com/Jeevithha/IMAGE-TRANSFORMATIONS/assets/123623197/db3a0122-fe98-4902-9d4a-a2c977758103)
### vi)Image Cropping
![315516938-f8bd26d8-a9f7-493d-9d13-0fad7272c3aa](https://github.com/Jeevithha/IMAGE-TRANSFORMATIONS/assets/123623197/60e64565-cc43-421c-95bd-d27f0983d11e)
![315516938-f8bd26d8-a9f7-493d-9d13-0fad7272c3aa](https://github.com/Jeevithha/IMAGE-TRANSFORMATIONS/assets/123623197/f40d5d88-6515-4b28-8914-4867a66dbf65)

## Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.

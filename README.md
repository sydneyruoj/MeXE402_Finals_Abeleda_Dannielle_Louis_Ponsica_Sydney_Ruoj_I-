# Converting Outdoor Surveillance Cameras Images to Grayscale
## Topic: Converting Images to Grayscale
Use the color space conversion code to convert RGB images to grayscale for basic image preprocessing.

## Dataset: [Outdoor CCTV Images](https://www.kaggle.com/datasets/ibrahimalobaid/day-and-night-image)

## Introduction
Converting Images to Grayscale is a fundamental preprocessing step in computer vision. Using the grayscale image, it simplifies the image data by reducing the number of color channels from three (RGB) *Red, Green, Blue* to one, making it easier to process and analyze. This technique is widely used in various applications, such as edge detection, object recognition, and image segmentation. Hence, this project highlights the use of converted grayscale images into outdoor surveillance camera images. For outdoor surveillance cameras, converting images to grayscale can help in detecting important details more easily.

## Abstract
This project shows how to change outdoor surveillance camera images to grayscale using OpenCV. The goal is to make the image data simpler for easier processing. The result will be grayscale images that keep the important details of the original color images.

## Project Methods
Here is the process of creating the project. We used the Google Colab in this project.

### Set up your working environment
First is to set up your working environment by cloning the repository, navigating to the correct directory, and clearing any unnecessary output. This setup is essential for working on your OpenCV projects efficiently.

```python
!git clone https://github.com/sydneyruoj/MeXE402_Finals_Abeleda_Dannielle_Louis_Ponsica_Sydney_Ruoj_I-
%cd OPenCV_Basics_Section_Abeleda-Dannielle-Louis_Ponsica-Sydney-Ruoj-I
from IPython.display import clear_output
clear_output()
```

### Import Libraries
Import the needed libraries, like OpenCV and NumPy.
```python
import cv2
from google.colab.patches import cv2_imshow
```

### Load Image
Use OpenCV to load the color image from a file.
```python
#This is the colorful image -=with 3 channels, RGB
image = cv2.imread("/content/MeXE402_Finals_Abeleda_Dannielle_Louis_Ponsica_Sydney_Ruoj_I-/images/day_1.jpg")
```
This prints the dimensions of the image. The output will show the height, width, and number of color channels (3 for RGB).
```python
print(image.shape)
```

### Convert to Grayscale
Change the loaded color image to grayscale using OpenCV's cvtColor function.
```python
gray = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
print(gray.shape)
```

### Display and Save Grayscale Image:
Show the grayscale image using OpenCV's imshow function and save it to a file.
```python
cv2_imshow(gray)
```

### HSV (Hue, Saturation, Value)
This is another step that can be integrated into converting images to grayscale. Though, it is not necessary to convert images to HSV before converting them to grayscale. You can directly convert the RGB image to grayscale without converting it to HSV first. The conversion to HSV is only needed if you plan to perform color-based operations before converting to grayscale

 **HSV (Hue, Saturation, Value)**:
   - Useful for color-based segmentation and analysis.
   - Separates color information (hue) from intensity (value), making it easier to work with colors.

```python
#HSV Image
HSV = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
print(HSV.shape)
cv2_imshow(HSV)

#grayscale image
gray = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
print(gray.shape)
cv2_imshow(gray)
```

## Conclusion
Converting images to grayscale is an important step in image processing. It makes the data simpler and highlights important details. This project shows how to do it using OpenCV with images from outdoor surveillance cameras.

## Additional Materials
### Code:
```python
!git clone https://github.com/sydneyruoj/MeXE402_Finals_Abeleda_Dannielle_Louis_Ponsica_Sydney_Ruoj_I-
%cd OPenCV_Basics_Section_Abeleda-Dannielle-Louis_Ponsica-Sydney-Ruoj-I
from IPython.display import clear_output
clear_output()
```

```python
import cv2
from google.colab.patches import cv2_imshow

#colorful image - 3 channels
image = cv2.imread("/content/MeXE402_Finals_Abeleda_Dannielle_Louis_Ponsica_Sydney_Ruoj_I-/images/day_1.jpg")
print(image.shape)

#HSV Image
HSV = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
print(HSV.shape)
cv2_imshow(HSV)

#grayscale image
gray = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
print(gray.shape)
cv2_imshow(gray)
```

### Images
### Results

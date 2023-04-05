# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import cv2, matplotlib.py libraries and display the saved images using cv2.imshow().

### Step2:
Use cv2.calcHist(images, channels, mask, histSize, ranges[, hist[, accumulate]]) to find the histogram of the image.

### Step3:
Plot the image and its stem plots using the plt.show() and plt.stem() functions.

### Step4:
Equalize the grayscale image using the in-built function cv2.equalizeHist().

### Step5:
Print the original and equalized image using cv2.imshow() and end the program.

# Program:
## Developed By:Sangeetha.K
## Register Number:212221230085
```
import cv2
import matplotlib.pyplot as plt
```
# Write your code to find the histogram of gray scale image and color image channels.
```
gray_img=cv2.imread('black.jpg')
color_img=cv2.imread('man.jpg')
plt.imshow(gray_img)
plt.show()
plt.imshow(color_img)
plt.show()
```

# Display the histogram of gray scale image and any one channel histogram from color image
### Histogram for Gray_scale_image
```
hist =cv2.calcHist([gray_img],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('graysczale val')
plt.xlabel('pixel count')
plt.stem(hist)
plt.show()
```
### Histogram for color_image
```
hist1 =cv2.calcHist([color_img],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('graysczale val')
plt.xlabel('pixel count')
plt.stem(hist1)
plt.show()
```


# Write the code to perform histogram equalization of the image. 

```
gray_img=cv2.imread('black.jpg',0)
equalize=cv2.equalizeHist(gray_img)
#Resizing image 
gray_img= cv2.resize(gray_img, (270,190))
equalize= cv2.resize(equalize, (270,190))
#Output
cv2.imshow('GRAY IMAGE',gray_img)
cv2.imshow('EQUALIZED IMAGE',equalize)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image

![Screenshot 2023-04-05 115331](https://user-images.githubusercontent.com/93992063/230105659-5dae0aeb-a96e-4f7e-9d5f-0230f50ad940.png)

### Histogram of Grayscale Image and any channel of Color Image

![Screenshot 2023-04-05 192706](https://user-images.githubusercontent.com/93992063/230105706-341aa651-f535-4532-bb8c-4a1b0754e5c1.png)
![Screenshot 2023-04-05 192752](https://user-images.githubusercontent.com/93992063/230105831-db24c55c-fa96-433a-96fb-63725707677a.png)

### Histogram Equalization of Grayscale Image

![Screenshot 2023-04-05 192903](https://user-images.githubusercontent.com/93992063/230105887-5832984f-bb35-4925-a96b-e350bf11af5c.png)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.

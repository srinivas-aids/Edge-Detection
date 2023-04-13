# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary packages matplolib and cv2.
<br>


### Step2:
Read the image as grayscale and reduce the noise using cv2.GaussianBlur.
<br>

### Step3:
Perform various methods of edge detection Sobel edge detector,Laplacian edge detector,Canny edge detector.
<br>

### Step4:
Run the program.
<br>

### Step5:

Execute the output.
 
## Program:

``` Python
Name : SRINIVAS.U 
REG-NO : 212221230108
# Import the packages
import cv2
import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise
image=cv2.imread('OIP.png')
gray=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
gaus=cv2.GaussianBlur(gray,(3,3),0)


# SOBEL EDGE DETECTOR
sobelx=cv2.Sobel(gaus,cv2.CV_64F,1,0,ksize=5)
sobely=cv2.Sobel(gaus,cv2.CV_64F,0,1,ksize=5)
sobelxy=cv2.Sobel(gaus,cv2.CV_64F,1,1,ksize=5)
plt.figure(1)
plt.subplot(2,2,1)
plt.imshow(gaus,cmap='gray')
plt.title('Original image')
plt.xticks([])
plt.yticks([])
plt.show()
#sobelx
plt.subplot(2,2,1)
plt.imshow(sobelx,cmap='gray')
plt.title('Sobelx')
plt.xticks([])
plt.yticks([])
plt.show()
#sobely
plt.subplot(2,2,1)
plt.imshow(sobely,cmap='gray')
plt.title('Sobely')
plt.xticks([])
plt.yticks([])
#sobelxy
plt.subplot(2,2,1)
plt.imshow(sobelxy,cmap='gray')
plt.title('Sobelxy')
plt.xticks([])
plt.yticks([])
plt.show()


# LAPLACIAN EDGE DETECTOR
laplacian = cv2.Laplacian(gaus,cv2.CV_64F)
plt.subplot(2,2,1)
plt.imshow(laplacian,cmap='gray')
plt.title('Laplacian edge detection')
plt.xticks([])
plt.yticks([])
plt.show()


# CANNY EDGE DETECTOR
canny_edges=cv2.Canny(gaus,120,150)
plt.subplot(2,2,1)
plt.imshow(canny_edges,cmap='gray')
plt.title('Canny edge detection')
plt.xticks([])
plt.yticks([])
plt.show()



```
## Output:
### IMAGE AFTER CONVERTING TO GRAYSCALE AND NOISE REMOVAL
<img width="227" alt="image" src="https://user-images.githubusercontent.com/93427183/231413255-7dc23090-954e-4d91-b155-e2e000b1d362.png">


### SOBEL EDGE DETECTOR

<img width="226" alt="image" src="https://user-images.githubusercontent.com/93427183/231413737-271073a3-437c-4c8f-b8ac-09c0f258046b.png">


<img width="206" alt="image" src="https://user-images.githubusercontent.com/93427183/231413666-c88a5aef-3117-4eb8-9b4d-377da394e77a.png">

<img width="217" alt="image" src="https://user-images.githubusercontent.com/93427183/231413857-ceb1ba21-e58f-49f2-8be7-2d6b8de2f700.png">



### LAPLACIAN EDGE DETECTOR

<img width="215" alt="image" src="https://user-images.githubusercontent.com/93427183/231413943-cf4ad695-a6ed-4c6e-974d-229452a6bb90.png">


### CANNY EDGE DETECTOR

<img width="203" alt="image" src="https://user-images.githubusercontent.com/93427183/231414021-068305a2-7cc8-4455-b23f-260ff0e3e31a.png">


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

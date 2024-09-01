# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

## Program:

### Developed By: B VIJAY
### Register Number: 212222230173
### i) Read and display the image:
```python
import cv2
image = cv2.imread('C:/Users/SEC/Downloads/31311aa (1) (1).jpg', 1)
if image is None:
    print("Error: Image not found. Please check the file path.")
else:
    image = cv2.resize(image, (200, 300))
    cv2.imshow('VIJAY', image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
### ii)Write the image:
```python
import cv2
image=cv2.imread('C:/Users/SEC/Downloads/31311aa (1) (1).jpg',0)
cv2.imwrite('31311aa (1) (1).jpg',image)
```
### iii)Shape of the Image:
```python
import cv2
image=cv2.imread('31311aa (1) (1).jpg',1)
print(image.shape)
```
### iv)Access rows and columns:
```python
import random
import cv2
image=cv2.imread('C:/Users/SEC/Downloads/31311aa (1) (1).jpg',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
  for j in range(image.shape[1]):
      image[i][j]=[random.randint(0,255),
                   random.randint(0,255),
                   random.randint(0,255)] 
cv2.imshow('part image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### v)Cut and paste portion of image:
```python
import cv2
image=cv2.imread('C:/Users/SEC/Downloads/31311aa (1) (1).jpg',1)
image=cv2.resize(image,(400,400))
tag =image[130:200,110:190]
image[110:180,120:200] = tag
cv2.imshow('partimage1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### vi) BGR and RGB to HSV and GRAY:
```python
import cv2
img = cv2.imread('C:/Users/SEC/Downloads/31311aa (1) (1).jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### vii) HSV to RGB and BGR:
```python
import cv2
img = cv2.imread('C:/Users/SEC/Downloads/31311aa (1) (1).jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### viii) RGB and BGR to YCrCb:
```python
import cv2
img = cv2.imread('C:/Users/SEC/Downloads/31311aa (1) (1).jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### ix) Split and merge RGB Image:
```python
import cv2
img = cv2.imread('C:/Users/SEC/Downloads/31311aa (1) (1).jpgg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### x) Split and merge HSV Image:
```python
import cv2
img = cv2.imread("C:/Users/SEC/Downloads/31311aa (1) (1).jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:

### i) Read and display the image

![Screenshot 2024-09-01 210948](https://github.com/user-attachments/assets/764990df-e75b-4c44-b5e2-7661111cc494)

<br>
<br>

### ii)Write the image

![image](https://github.com/user-attachments/assets/5ebfe8a5-0d30-4cef-b988-1fb791fdd69d)

<br>
<br>
  
### iii)Shape of the Image

![image](https://github.com/user-attachments/assets/4be176c2-2c0e-4317-b466-b853593ef097)

<br>
<br>

### iv)Access rows and columns

![Screenshot 2024-09-01 212732](https://github.com/user-attachments/assets/319ba679-1fa9-49e8-b00d-7400f040fbab)

<br>
<br>

### v)Cut and paste portion of image

![Screenshot 2024-09-01 212942](https://github.com/user-attachments/assets/ca0e51e8-960a-45ac-bca4-089ea58193a4)

<br>
<br>

### vi) BGR and RGB to HSV and GRAY

![Screenshot 2024-09-01 213102](https://github.com/user-attachments/assets/0b22bd93-6378-449d-ad18-c8fedb4a875a)

<br>
<br>

### vii) HSV to RGB and BGR


![Screenshot 2024-09-01 213241](https://github.com/user-attachments/assets/ee102d82-ad0c-4f64-a0b8-4ed92de1a217)

<br>
<br>

### viii) RGB and BGR to YCrCb

![Screenshot 2024-09-01 213349](https://github.com/user-attachments/assets/688df0a0-81c1-44f2-af81-02efb5b0a8be)

<br>
<br>

### ix) Split and merge RGB Image

![Screenshot 2024-09-01 213503](https://github.com/user-attachments/assets/c5b9cf61-fd59-4efc-8980-e6e1520ab09f)

<br>
<br>

### x) Split and merge HSV Image

![Screenshot 2024-09-01 213628](https://github.com/user-attachments/assets/f8fe41a9-7b17-4979-8bcb-43e4c3c0abf4)

<br>
<br>




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.








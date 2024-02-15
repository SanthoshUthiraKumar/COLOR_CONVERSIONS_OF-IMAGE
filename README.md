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
### Step1: Choose an image and save it as a filename.jpg ,
### Step2: Use imread(filename, flags) to read the file.
### Step3: Use imshow(window_name, image) to display the image.
### Step4: Use imwrite(filename, image) to write the image.
### Step5: End the program and close the output image windows.
### Step6: Convert BGR and RGB to HSV and GRAY
### Step7: Convert HSV to RGB and BGR
### Step8: Convert RGB and BGR to YCrCb
### Step9: Split and Merge RGB Image
### Step10: Split and merge HSV Image

##### Program:
```
### Developed By: Santhosh U
### Register Number: 212222240092
```
<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
    import cv2
    image=cv2.imread('Dipt_1.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('Santhosh',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:

 <img src="https://github.com/SanthoshUthiraKumar/COLOR_CONVERSIONS_OF-IMAGE/assets/119477975/f2c9122b-ea14-447b-821f-b3f3449df321">
  </td>
  </tr>

   <tr>
    <td width=50%>

### ii)Write the image
```Python
    import cv2
    image=cv2.imread('Dipt_1.jpg',0)
    cv2.imwrite('demo.jpg',image)
```
  </td>
  <td>

### OUTPUT:

<img src="https://github.com/SanthoshUthiraKumar/COLOR_CONVERSIONS_OF-IMAGE/assets/119477975/4b5421c9-6e1f-4f69-8f85-be3c1eaa6581">
  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```Python
    import cv2
    image=cv2.imread('Dipt_1.jpg',1)
    print(image.shape)
```
  </td>
  <td>

### OUTPUT:

<img src="https://github.com/SanthoshUthiraKumar/COLOR_CONVERSIONS_OF-IMAGE/assets/119477975/13811ac2-b467-4b84-a481-bafe937567e9">
  </td>
  </tr>
  <tr>
    <td>
      
### iv)Access rows and columns
```Python
    import random
    import cv2
    image=cv2.imread('Dipt_1.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
        for j in range(image.shape[1]):
            image[i][j]=[random.randint(0,255),
                        random.randint(0,255),
                        random.randint(0,255)] 
    cv2.imshow('part_img',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td width="50%">

### OUTPUT:

 <img src="https://github.com/SanthoshUthiraKumar/COLOR_CONVERSIONS_OF-IMAGE/assets/119477975/ae10c159-1e6a-4056-b409-7b736be3c0cf">
  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v)Cut and paste portion of image

 ```Python
    import cv2
    image=cv2.imread('Dipt_1.jpg',1)
    image=cv2.resize(image,(400,400))
    tag =image[130:200,110:190]
    image[110:180,120:200] = tag
    cv2.imshow('part_img_1',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td>
    
### OUTPUT:

<img src="https://github.com/SanthoshUthiraKumar/COLOR_CONVERSIONS_OF-IMAGE/assets/119477975/18270de8-ba72-4e56-9f2b-d13149ee786b">
  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```Python
import cv2
img = cv2.imread('Dipt_1.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Og_Img',img)
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

### OUTPUT:
![out6](https://github.com/SanthoshUthiraKumar/COLOR_CONVERSIONS_OF-IMAGE/assets/119477975/372fa91f-c7ad-48b5-8605-2a91cf561631)

### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('Dipt_1.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Og HSV Image',img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![out7](https://github.com/SanthoshUthiraKumar/COLOR_CONVERSIONS_OF-IMAGE/assets/119477975/fef3efa7-dd7f-46fc-851a-cc349fe6f27b)

### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('Dipt_1.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![out8](https://github.com/SanthoshUthiraKumar/COLOR_CONVERSIONS_OF-IMAGE/assets/119477975/94b30e27-9343-4d8b-a9fc-cd68afe8a646)

### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('Dipt_1.jpg',1)
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

### OUTPUT:
![out9](https://github.com/SanthoshUthiraKumar/COLOR_CONVERSIONS_OF-IMAGE/assets/119477975/f3550cfc-099f-451a-80e1-da3239116b4a)

### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("Dipt_1.jpg",1)
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

### OUTPUT:
![out10](https://github.com/SanthoshUthiraKumar/COLOR_CONVERSIONS_OF-IMAGE/assets/119477975/12131c51-7fd4-42aa-8207-19c98048ef57)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.

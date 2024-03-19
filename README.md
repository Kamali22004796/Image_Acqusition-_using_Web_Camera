# Image_Acqusition-_using_Web_Camera
## Aim
 
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
<br>

### Step 2:
<br>

### Step 3:
<br>

### Step 4:
<br>

### Step 5:
<br>

## Program:
### Developed By: Kamali E
### Register No: 212222110015

## i) Write the frame as JPG file
```
import cv2
obj = cv2.VideoCapture(0)
while(True):
    cap,frame = obj.read()
    cv2.imshow('video.jpg',frame)
    cv2.imwrite("oscar.jpg",frame)
    if cv2.waitKey(1) == ord('q'):
        break
obj.release()
```

## ii) Display the video
```
import cv2
img = cv2.VideoCapture(0)
while(True):
    imagee,frame = img.read()
    cv2.imshow('OSCAR',frame)
    cv2.imwrite("MY_OSCAR.jpg",frame)
    if cv2.waitKey(1) == ord('q'):
        break
img.release()
cv2.destroyAllWindows()

```

## iii) Display the video by resizing the window
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('OSCAR ',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```




## iv) Rotate and display the video

import cv2
import numpy as np
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read() 
    width = int(cap.get(3))
    height = int(cap.get(4))
    image = np.zeros(frame.shape, np.uint8) 
    smaller_frame = cv2.resize(frame, (0,0), fx = 0.5, fy=0.5)
    image[:height//2, :width//2] = cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2] = smaller_frame 
    image[:height//2, width//2:] = smaller_frame
    image[height//2:, width//2:] = cv2.rotate(smaller_frame,cv2.ROTATE_180)
    cv2.imshow('OSCAR', image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output

### i) Write the frame as JPG image

![312689231-dd014573-9828-4cd2-a37c-633c95763550](https://github.com/Kamali22004796/Image_Acqusition-_using_Web_Camera/assets/120567837/8c147d17-3048-4983-9e4c-0d0dcf8a741b)




### ii) Display the video

![312689280-61ab2e72-b69a-4740-9f3c-f5962ce08365](https://github.com/Kamali22004796/Image_Acqusition-_using_Web_Camera/assets/120567837/a893b2df-56b8-4ad6-b7d6-a1fb6c7b5cdb)



### iii) Display the video by resizing the window

![312689307-eaf8fdfd-b98a-4ae6-89b7-7a4ba6167be3](https://github.com/Kamali22004796/Image_Acqusition-_using_Web_Camera/assets/120567837/8101c748-1fda-4f45-b841-85290c00125c)





### iv) Rotate and display the video

![312689329-b18e56aa-82f9-4785-b40d-a88ed04c701c](https://github.com/Kamali22004796/Image_Acqusition-_using_Web_Camera/assets/120567837/8fd4cd9f-1181-4738-a210-1ae2a1161a69)





## Result:
Thus the image is accessed from webcamera and displayed using openCV.

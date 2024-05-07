# 2. Image_Acqusition-_using_Web_Camera


## Aim
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Use cv2.VideoCapture(0) to access web camera

### Step 2:
Use cv2.imread to read the video or image

### Step 3:
Use cv2.imwrite to save the image

### Step 4:
Use cv2.imshow to show the video

### Step 5:
Use cv2.imshow to show the video

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
```
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


![312689231-dd014573-9828-4cd2-a37c-633c95763550](https://github.com/Kamali22004796/Image_Acqusition-_using_Web_Camera/assets/120567837/e66fb8f6-819d-4333-a6f3-bb6afe06819c)


### ii) Display the video

![312689280-61ab2e72-b69a-4740-9f3c-f5962ce08365](https://github.com/Kamali22004796/Image_Acqusition-_using_Web_Camera/assets/120567837/36001f81-2f1a-4252-973f-c527c6e22062)


### iii) Display the video by resizing the window

![312689307-eaf8fdfd-b98a-4ae6-89b7-7a4ba6167be3](https://github.com/Kamali22004796/Image_Acqusition-_using_Web_Camera/assets/120567837/21da2c0e-3212-474b-8ffd-f15ec36b8ac2)


### iv) Rotate and display the video

![312689329-b18e56aa-82f9-4785-b40d-a88ed04c701c](https://github.com/Kamali22004796/Image_Acqusition-_using_Web_Camera/assets/120567837/a547db69-2c78-4945-82a1-77dc8d16c44a)



## Result:
Thus the image is accessed from webcamera and displayed using openCV.

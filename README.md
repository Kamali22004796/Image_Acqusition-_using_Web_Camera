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

![Screenshot 2024-03-27 104142](https://github.com/Kamali22004796/Image_Acqusition-_using_Web_Camera/assets/120567837/63b2b8ad-a6f0-4cca-ade4-46ae25164141)

### ii) Display the video
![309529523-9b69cdfa-bcfb-47b9-90a7-999eeed92611](https://github.com/Kamali22004796/Image_Acqusition-_using_Web_Camera/assets/120567837/df972618-d7ee-4173-910e-d58191afe151)



### iii) Display the video by resizing the window

![309529527-659e9135-1380-4528-8a34-015ef481171b](https://github.com/Kamali22004796/Image_Acqusition-_using_Web_Camera/assets/120567837/22e92e13-fc80-4df0-94ee-8ff4b16dbf7b)


### iv) Rotate and display the video

![309529539-117d9e88-73dc-4389-855b-1bbb9fc627ef](https://github.com/Kamali22004796/Image_Acqusition-_using_Web_Camera/assets/120567837/c706c65f-0a27-4670-8a72-d24de2c910ae)



## Result:
Thus the image is accessed from webcamera and displayed using openCV.

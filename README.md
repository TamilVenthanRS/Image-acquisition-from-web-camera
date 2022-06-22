# Image-Acquisition-from-Web-Camera
## Aim:
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:

Use VideoCapture(0) to access web camera.
### Step 2:

Use imread to read the video or image.
### Step 3:

Use imshow to show the video.
### Step 4:

Use imshow to show the video.
### Step 5:

End the program and close the output video windows by pressing 'q'.
## Program:
``` Python
### Developed By:Tamil venthan R S
### Register No:212220230054
## i) Write the frame as JPG file
import cv2
videoCaptureObject = cv2.VideoCapture(0)
while(True):
    ret,frame = videoCaptureObject.read()
    cv2.imshow("apple.jpg",frame)
    result = False
videoCaptureObject.release()
cv2.destroyAllWindows()
## ii) Display the video
import cv2
import numpy as np
cap = cv2.VideoCapture(0)
while True:
    ret,frame = cap.read()
    cv2.imshow('frame', frame)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
## iii) Display the video by resizing the window
import cv2
import numpy as np
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape, np.uint8)
    smaller_frame=cv2.resize(frame, (0,0), fx=0.5, fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('frame', image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
## iv) Rotate and display the video
import cv2
import numpy as np
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape, np.uint8)
    smaller_frame=cv2.resize(frame, (0,0), fx=0.5, fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('frame', image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output
### i) Write the frame as JPG image

![ 2022-04-11 ](https://user-images.githubusercontent.com/75235477/162872795-396d0ada-23fe-4077-a5ae-03e4f4f3f724.jpeg)

### ii) Display the video

![2022-04-11  (3)](https://user-images.githubusercontent.com/75235477/162872869-402f6e41-3b20-42f3-8d98-1b83d51a3cde.jpeg)
### iii) Display the video by resizing the window

![ 2022-04-11 ](https://user-images.githubusercontent.com/75235477/162872955-f4a7c339-e0f5-4a13-b3f5-ce6ab6953a07.jpeg)

### iv) Rotate and display the video

![ 2022-04-11 ](https://user-images.githubusercontent.com/75235477/162872961-bf2e68c0-717f-4452-8c85-bf020c7f5568.jpeg)

## Result:
Thus the image is accessed from webcamera and displayed using openCV.

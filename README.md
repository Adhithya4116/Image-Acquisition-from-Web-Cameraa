# Image-Acquisition-from-Web-Cameraa
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
Use cv2.VideoCapture(0) to access web camera
<br>

### Step 2:
Use cv2.imread to read the video or image
<br>

### Step 3:
Use cv2.imwrite to save the image
<br>

### Step 4:
Use cv2.imshow to show the video
<br>

### Step 5:
End the program and close the output video window by pressing 'q'.
<br>

## Program:
``` Python
### Developed By: Adhithya Perumal.D
### Register No:  212222230007

## i) Write the frame as JPG file

import cv2
videoCaptureObject = cv2.VideoCapture(0)
while(True):
    ret,frame = videoCaptureObject.read()
    cv2.imshow('DAP',frame)
    if cv2.waitKey(1) == ord('q'):
        break
videoCaptureObject.release()
cv2.destroyAllWindows()




## ii) Display the video

import cv2
videoCaptureObject = cv2.VideoCapture(0)
while(True):
    ret,frame = videoCaptureObject.read()
    cv2.imshow('DAP',frame)
    if cv2.waitKey(1) == ord('q'):
        break
videoCaptureObject.release()
cv2.destroyAllWindows()



## iii) Display the video by resizing the window

import cv2
import numpy as np
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read() 
    width = int(cap.get(3))
    height = int(cap.get(4))
    image = np.zeros(frame.shape, np.uint8) 
    smaller_frame = cv2.resize(frame, (0,0), fx = 0.5, fy=0.5) 
    image[:height//2, :width//2] = smaller_frame
    image[height//2:, :width//2] = smaller_frame
    image[:height//2, width//2:] = smaller_frame 
    image [height//2:, width//2:] = smaller_frame
    cv2.imshow('DAP', image)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()






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
    image[height//2:, :width//2] = cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[:height//2, width//2:] = smaller_frame 
    image [height//2:, width//2:] = smaller_frame
    cv2.imshow('DAP', image)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()








```
## Output

### i) Write the frame as JPG image
![Screenshot 2024-03-06 234725](https://github.com/Adhithya4116/Image-Acquisition-from-Web-Cameraa/assets/118707079/29b4d5e5-5489-446c-8262-a7de79bf844f)

</br>
</br>


### ii) Display the video
![Screenshot 2024-03-06 235426](https://github.com/Adhithya4116/Image-Acquisition-from-Web-Cameraa/assets/118707079/8260883b-22bb-4449-a171-3a76e8c37a4b)

</br>
</br>


### iii) Display the video by resizing the window
![Screenshot 2024-03-06 235535](https://github.com/Adhithya4116/Image-Acquisition-from-Web-Cameraa/assets/118707079/c52a9fd7-6cb1-4ba7-bf7a-3b3f43c2317d)

</br>
</br>



### iv) Rotate and display the video
![Screenshot 2024-03-06 235625](https://github.com/Adhithya4116/Image-Acquisition-from-Web-Cameraa/assets/118707079/1518df9d-81ab-47f6-988d-b2c6bb68f9f7)

</br>
</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.

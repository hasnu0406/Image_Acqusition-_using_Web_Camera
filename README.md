# Image_Acqusition-_using_Web_Camera
## Name: HASNA MUBARAK AZEEM
## Register no: 212223240052

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
Import OpenCV Package.

### Step 2:
Capture Video from Webcam. Use VideoCapture(0) to access the webcam and start capturing video.

### Step 3:
Read Video or Image. Utilize 'imread' to read a video frame or image from the webcam.

### Step 4:
Save Image to File. Employ 'imwrite' to save the captured image to a file.

### Step 5:
Display Video or Image. Use 'imshow' to display the captured video frame or image.

### Step 6:
End Program with 'q'. Allow the program to be terminated by pressing the 'q' key.


## Program:
### Developed By: SAJITH AHAMED F
### Register No: 212223240144


## i) Write the frame as JPG file

```
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("HASNA.jpg", frame)
cap.release()
captured_image = cv2.imread('HASNA.jpg')
plt.imshow(captured_image[:,:,::-1])
plt.axis('off')
plt.show()
```


## ii) Display the video

```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```


## iii) Display the video by resizing the window

```

cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  # Resize to 320x240
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
  

```


## iv) Rotate and display the video

```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release() 
```

## Output

### i) Write the frame as JPG image
<img width="733" height="550" alt="image" src="https://github.com/user-attachments/assets/8cf81617-b70d-4c98-a265-641fae8820cd" />




### ii) Display the video
<img width="739" height="553" alt="image" src="https://github.com/user-attachments/assets/abd9c9b4-c156-4420-b3e5-d3f20de0d069" />





### iii) Display the video by resizing the window
<img width="366" height="553" alt="image" src="https://github.com/user-attachments/assets/e4fcc6d9-8d57-4dc1-8658-a3d5e3e07ef4" />








### iv) Rotate and display the video
<img width="414" height="554" alt="image" src="https://github.com/user-attachments/assets/eb30837a-ab38-4565-8de9-ae6515c36707" />





## Result:
Thus the image is accessed from webcamera and displayed using openCV.

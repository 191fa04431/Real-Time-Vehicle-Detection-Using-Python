# [Real-time-Vehicle-Dection-Using-Python]

Hi guys, This repository consists of a source code of the script to detect cars in a video/camera frame and then draw rectangular boxes around them.

The **ML algorithms** used for detecting cars and bounding box coordinates is a pre-trained cascade model [Haarcascade car] 

## Getting started

Firstly we have to clone the project repository or download the zip of the project and then extract it.

```bash
git clone https://github.com/191fa04431/Real-Time-Vehicle-Detection-Using-Python.git
cd Real-time-Vehicle-Detection-Python
Real-time-Vehicle-Detection-Python ->
```

## Dependencies

Now once we have the project repo in our local directory, now lets install the dependecies required to run our script

```bash
pip install opencv-python
```

## Sample video

The sample video we used in this project is [**cars.mp4**], which will come as you download or clone the repository, to load a different video with a different filename, you might wanna change the source code a bit.

```python
def Simulator():
    CarVideo = cv2.VideoCapture('cars.mp4') # change cars.mp4 to name of your video
    while CarVideo.isOpened():
        ret, frame = CarVideo.read()
        controlkey = cv2.waitKey(1)
        if ret:        
            cars_frame = detect_cars(frame)
            cv2.imshow('frame', cars_frame)
        else:
            break
        if controlkey == ord('q'):
            break

    CarVideo.release()
    cv2.destroyAllWindows()

```

## Issues ?

Are you facing any issue while trying to run the script, well then raise an issue and I will do my best fixing it as soon as I can


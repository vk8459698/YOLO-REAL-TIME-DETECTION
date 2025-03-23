# Real-Time Object Detection

## Overview
This project performs real-time object detection using OpenCV's deep learning module (`cv2.dnn`). The model used is **MobileNet SSD**, which can detect multiple object classes in a video stream.

## Installation
### Requirements
Ensure you have the following dependencies installed:
```sh
pip install numpy opencv-python imutils
```

## Usage
Run the following command to start real-time object detection:
```sh
python real_time_object_detection.py
```

## How It Works
1. Loads the trained **MobileNet SSD** model.
2. Captures video frames from the webcam.
3. Preprocesses frames and runs them through the neural network.
4. Identifies objects and draws bounding boxes with labels and confidence scores.
5. Displays the real-time detection results.

## Model and Configuration Files
Ensure the following files are present:
- `MobileNetSSD_deploy.prototxt.txt` (Model architecture definition)
- `MobileNetSSD_deploy.caffemodel` (trained model weights)

## Controls
- Press `q` to quit the program.

## Example Output
Objects detected in the webcam stream are highlighted with bounding boxes and labeled with their respective class names and confidence scores.

## Classes Detected
The model can detect:
- Person
- Car
- Bicycle
- Dog
- Cat
- And many more (see `CLASSES` list in the code)

---
### Author
Vivek Kumar

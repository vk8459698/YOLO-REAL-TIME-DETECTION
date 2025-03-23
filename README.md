# YOLO-object-detection-with-OpenCV
Object detection using YOLO object detector

### Detect objects in both images and video streams using Deep Learning, OpenCV, and Python.

I am  using YOLOv3 in this project, in particular, YOLO trained on the COCO dataset.

The COCO dataset consists of 80 labels, including, but not limited to:

- People
- Bicycles
- Cars and trucks
- Airplanes
- Stop signs and fire hydrants
- Animals, including cats, dogs, birds, horses, cows, and sheep, to name a few
- Kitchen and dining objects, such as wine glasses, cups, forks, knives, spoons, etc.
…and much more!


- yolo-coco : The YOLOv3 object detector trained (on the COCO dataset) model files.



## Screenshots
![Image](/Object%20dection%20using%20image/1.png)

Here you can see that YOLO has not only detected each person in the input image, but also the suitcases as well!

Furthermore, if you take a look at the right corner of the image you’ll see that YOLO has also detected the handbag on the lady’s shoulder.

<img src="https://github.com/yash42828/YOLO-object-detection-with-OpenCV/blob/master/Object%20dection%20using%20image/2.png">

YOLO is able to correctly detect each of the players on the pitch, including the soccer ball itself. Notice the person in the background who is detected despite the area being highly blurred and partially obscured.


## Limitation:
### Arguably the largest limitation and drawback of the YOLO object detector is that:

- It does not always handle small objects well
- It especially does not handle objects grouped close together
- The reason for this limitation is due to the YOLO algorithm itself:

The YOLO object detector divides an input image into an SxS grid where each cell in the grid predicts only a single object.
If there exist multiple, small objects in a single cell then YOLO will be unable to detect them, ultimately leading to missed object detections.
Therefore, if you know your dataset consists of many small objects grouped close together then you should not use the YOLO object detector.

In terms of small objects, Faster R-CNN tends to work the best; however, it’s also the slowest.

SSDs can also be used here; however, SSDs can also struggle with smaller objects (but not as much as YOLO).

SSDs often give a nice tradeoff in terms of speed and accuracy as well.

## Real-time object detection with deep learning and OpenCV

## Installation

- `pip install numpy`
- `pip install opencv-python`
- `pip install imutils`

## To Run the project

- `python real_time_object_detection.py`

## Screenshots
<img src="https://github.com/yash42828/YOLO-object-detection-with-OpenCV/blob/master/real-time-object-detection/real_time.gif">

Notice how our deep learning object detector can detect not only a person, but also the sofa and the chair next to person — all in real-time!


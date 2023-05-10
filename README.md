RBE 549: Computer Vision
Team members: Deepak Nagle, Irakli Gregolia
Project 3: Perception Stack: Einstein Vision
 
Networks utilized:
1. Object detection (cars, traffic signs, traffic lights, speed limit sign):
We used this one for object detection: https://github.com/xiaogangLi/tensorflow-MobilenetV1-SSD
We found midpoints of the cars, traffic signs, traffic lights using the bounding boxes obtained from this network by feeding it the images.
However, next time, we plan on using instance/panoptic segmentation network in hopes that it will 
provide better results for depth estimation (using average depth in the segmented part of the image)

2. Depth estimation:
We used transformer based midas: https://github.com/jankais3r/Video-Depthify
We took the bounding boxes from object detection and found average depths in the same regions as those
of bounding boxes to obtain estimated depths. However, we expect to use instance segmentation instead of 
object detection for better results.

3. Lane detection:
YOLO Pv2 : https://github.com/CAIC-AD/YOLOPv2
Detected the lanes through this network.

Note: We were able to detect all 6 classes, however, in case of the speed limit sign, we could detect it,
we were able to place a speed limit sign of the rendering, but we could not project "Speed_Limit_blank_sign.svg"
thing on that speed limit sign that we rendered. This was because the file was in .svg instead of .png and blender
does not take .svg images. While converting it to .png, the image was getting distorted and there were a lot of issues. 
This issue did not occur with the stop sign image as that was in .png format.
However, we did render all the 6 classes. Just that in case of speed limit, we could not project the image text on the
projected speed limit sign.

Thank you!
 
[2] Lane Detection: https://github.com/IrohXu/lanenet-lane-detection-pytorch
[3] Monocular Depth Estimation: https://github.com/isl-org/MiDaS
[4] Object Detection: Cars, Trucks, Traffic Lights, Road Signs:
https://github.com/xiaogangLi/tensorflow-MobilenetV1-SSD
[5] Object Detection: Cars, Trucks, Traffic Lights, Road Signs:
https://github.com/WongKinYiu/yolov7
[6] Object Detection: Traffic Lights: https://github.com/sovit-123/TrafficLight-Detection-Using-YOLOv3
[7] Object Detection: Road Signs: https://github.com/Anantmishra1729/Road-sign-detection
[8] YOLO 3-D bounding boxes: https://github.com/ruhyadi/YOLO3D
[9] Pedestrian keypoint detection: https://github.com/ZheC/Realtime MultiPerson Pose Estimation
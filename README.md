# kinect2_calibration
Kinect V2 QHD camera calibration.


Step1. Change camera to edit code.


Open src/kinect2_calibration.cpp file.


Find line 1349 in code.


---if use HD camera.


------then std::string topicColor = "/" + ns + K2_TOPIC_HD + K2_TOPIC_IMAGE_MONO;

---if use QHD camera.


------std::string topicColor = "/" + ns + K2_TOPIC_QHD + K2_TOPIC_IMAGE_MONO;


Step2. Run Kinect V2 camera calibration.
``` bash
$ rosrun kinect2_calibration kinect2_calibration
```

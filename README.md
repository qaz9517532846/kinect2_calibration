# kinect2_calibration
Kinect V2 QHD camera calibration.

Need download [iai_kinect2](https://github.com/code-iai/iai_kinect2) .

Step1. Change camera to edit code.


Step2. Open kinect2_calibration/src/kinect2_calibration.cpp file.


Step3. Find line 1349 in code.


   if use HD camera.


------then std::string topicColor = "/" + ns + K2_TOPIC_HD + K2_TOPIC_IMAGE_MONO;

---if use QHD camera.


------then std::string topicColor = "/" + ns + K2_TOPIC_QHD + K2_TOPIC_IMAGE_MONO;

Step4. Find line 496 in code.


---if use HD camera.


------then sizeColor(1080, 960);

---if use QHD camera.


------then sizeColor(960, 540);

Step5. return ros workspace.
``` bash
$ cd <ros workspace>
```

``` bash
$ catkin_make
```

Step6. Run Kinect V2 camera calibration.
``` bash
$ rosrun kinect2_calibration kinect2_calibration
```

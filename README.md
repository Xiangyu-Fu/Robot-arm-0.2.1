# Robot-arm-0.2.1
> **notice**：These files have not been secondary confirmed！I can only be sure that they can work properly in my environment.

In this version, the robot arm can recognize and clip the target
Run the program and add the target.Note that the target is not included in this library.
```
$ cd ~/catkin_ws
$ source devel/setup.bash
$ roslaunch arm1 gazebo.launch
```
run the image processing node.
For program logic reasons,the image processing node should be run first.
Otherwise, the program will not run.
```
$ cd ~/catkin_ws
$ source devel/setup.bash
$ rosrun arm1 image_process
```
run the logical controller node.
```
$ cd ~/catkin_ws
$ source devel/setup.bash
$ rosrun arm1 arm_command
```
View the rgb-camera topic
```
rqt_image_view /rgb_camera/image_raw
```
for example:
![example](https://img-blog.csdnimg.cn/20200401013234345.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM3MjY2OTE3,size_16,color_FFFFFF,t_70)
![gif](https://img-blog.csdnimg.cn/20200416064126290.gif)
# 06.APR.2020 Updates
Updated the solidworks file of the robot. Not sure if arm0.1.SLDASM can be opened, you may need to find the file again.

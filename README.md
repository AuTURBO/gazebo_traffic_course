
# image shot
<img src="/picture/1.png" width="70%" height="70%">
<img src="/picture/2.png" width="70%" height="70%">
<img src="/picture/3.png" width="70%" height="70%">

# youtube video
traffic light operating , Click image to link to YouTube video.   
[![Video Label](http://img.youtube.com/vi/_JnlcazSEME/0.jpg)](https://youtu.be/_JnlcazSEME?t=0s)  
traffic bar operating , Click image to link to YouTube video.  
[![Video Label](http://img.youtube.com/vi/abc1jvPWbP8/0.jpg)](https://youtu.be/abc1jvPWbP8?t=0s)  

# Run
I made it based on RBIZ 2017 autorace stadium

* First install TurtleBot3 package
http://emanual.robotis.com/docs/en/platform/turtlebot3/pc_setup/#pc-setup

```bash
$ sudo apt-get install ros-kinetic-joy ros-kinetic-teleop-twist-joy ros-kinetic-teleop-twist-keyboard ros-kinetic-laser-proc ros-kinetic-rgbd-launch ros-kinetic-depthimage-to-laserscan ros-kinetic-rosserial-arduino ros-kinetic-rosserial-python ros-kinetic-rosserial-server ros-kinetic-rosserial-client ros-kinetic-rosserial-msgs ros-kinetic-amcl ros-kinetic-map-server ros-kinetic-move-base ros-kinetic-urdf ros-kinetic-xacro ros-kinetic-compressed-image-transport ros-kinetic-rqt-image-view ros-kinetic-gmapping ros-kinetic-navigation ros-kinetic-interactive-markers

$ cd ~/catkin_ws/src/
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3.git
$ cd ~/catkin_ws && catkin_make
```

* Second install turtlebot3_traffic_course package
```bash
 $ cd ~/catkin_ws/src/
 $ git clone https://github.com/AuTURBO/gazebo_traffic_course.git
 $ cd ~/catkin_ws && catkin_make
```
* Add Camera to turtlebot3 burger simulation model. 
```bash
 Default turtlebot3 burger simulation model don't support camera and depth camera.
 If you wand to add camera and depth camera to turtlebot3 burger simulation model, 
 you modify turtlebot3_burger.gazebo.xacro  and turtlebot3_burger.urdf.xacro
 $ cp ~/catkin_ws/src/gazebo_traffic_course/burger_camera/turtlebot3_burger.gazebo.xacro ~/catkin_ws/src/turtlebot3/turtlebot3_description/urdf/
 $ cp ~/catkin_ws/src/gazebo_traffic_course/burger_camera/turtlebot3_burger.urdf.xacro ~/catkin_ws/src/turtlebot3/turtlebot3_description/urdf/
```
* Run Gazebo World
```bash
 If you want turtlebot3 burger. Simulation lane width is 30 cm.  
 $ roslaunch turtlebot3_traffic_course course_burger.launch
```
```bash
 If you want turtlebot3 waffle. Simulation lane width is 40 cm.  
 $ roslaunch turtlebot3_traffic_course course_waffle.launch
```
* Run control, you can contol turtlebot3 model at gazebo simulation world
```bash
 $ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```

# Build

* plugin build to control traffic light and bar.
```bash
 $ cd ~/catkin_ws/src/gazebo_traffic_course/gazebo_plugin_tutorial/build
 $ cmake ../
 $ make
```


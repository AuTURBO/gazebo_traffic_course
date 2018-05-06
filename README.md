
# image shot click
<img src="/picture/1.png" width="70%" height="70%">
<img src="/picture/2.png" width="70%" height="70%">
<img src="/picture/3.png" width="70%" height="70%">
# youtube video click
traffic light operating  
[![Video Label](http://img.youtube.com/vi/_JnlcazSEME/0.jpg)](https://youtu.be/_JnlcazSEME?t=0s)  
traffic bar operating  
[![Video Label](http://img.youtube.com/vi/abc1jvPWbP8/0.jpg)](https://youtu.be/abc1jvPWbP8?t=0s)  

# Run
I made it based on RBIZ 2017 autorace stadium\

* First install TurtleBot3 package
http://emanual.robotis.com/docs/en/platform/turtlebot3/pc_setup/#pc-setup

* Second install turtlebot3_simulation package
```bash
 $ cd ~/catkin_ws/src/
 $ git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
 $ cd ~/catkin_ws && catkin_make
```

* Third install turtlebot3_traffic_course package
```bash
 $ cd ~/catkin_ws/src/
 $ git clone https://github.com/hyunoklee/turtlebot3_traffic_course.git
 $ cd ~/catkin_ws && catkin_make
```
* turtlebot model3 setting and run
```bash
 If you want turtlebot3 burger. Simulation lane width is 30 cm. 
 but turtlebot3 burger simulation model don't have camera. 
 $ roslaunch turtlebot3_traffic_course course_burger.launch
```
```bash
 If you want turtlebot3 waffle. Simulation lane width is 40 cm.  
 and turtlebot3 waffle simulation model have camera and depth camera.  
 $ roslaunch turtlebot3_traffic_course course_waffle.launch
```
* control run , you can contol turtlebot3 model at gazebo simulation world
```bash
 $ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```

# Build

* plugin build 
```bash
 $ cd ~/catkin_ws/src/gazebo_traffic_course/gazebo_plugin_tutorial/build
 $ cmake ../
 $ make
```


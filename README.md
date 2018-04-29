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
* turtlebot model3 setting
```bash
 $ sudo gedit ~/.bashrc
 If you want turtelbot3 waffle , write below at .bashrc 
 export TURTLEBOT3_MODEL=waffle 
 If you want turtelbot3 burger , write below at .bashrc 
 export TURTLEBOT3_MODEL=burger
 $ source ~/.bashrc
```
* simulation run
```bash
 $ roslaunch turtlebot3_traffic_course course.launch
```

* control run , you can contol turtlebot3 model at gazebo simulation world
```bash
 $ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```

<img src="/picture/1.png" width="70%" height="70%">
<img src="/picture/2.png" width="70%" height="70%">
<img src="/picture/3.png" width="70%" height="70%">


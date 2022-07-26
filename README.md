Install arduino robot arm packages to control robot arm with Moveit and Rviz

# Install_arduino_robot_Arm
###  1- First install catkin:
```

 sudo apt-get install ros-noetic-catkin
```


### 2- Change the dict to catkin's source
```
 mkdir -p ~/catkin_ws/src
```
```
 cd ~/catkin_ws/
```
```
 catkin_make
```



### 3- Install git and conncet to github repostary
```
 cd ~/catkin_ws/src
```
```
 sudo apt install git
```
```
 git clone https://github.com/smart-methods/arduino_robot_arm
```
```
 cd ~/catkin_ws
```



### 4- Install and initilzie rosdep 
```
 sudo apt install python3-rosdep2
```
```
 rosdep install --from-paths src --ignore-src -r -y
```


### 5- Install depandacies 
```
 sudo apt-get install ros-noetic-moveit
```
```
 sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
```
```
 sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
```
```
 sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
```



### 6- Follow the commands 
```
 sudo nano ~/.bashrc
```
go to the last line then add this command:

**#instead of 'your name' write your user name**
```
source /home/your name/catkin_ws/devel/setup.bash
```

***


# Install arduino
**Arduino IDE in Ubuntu https://www.arduino.cc/en/software**

### 1- Follow the commands 
```
 sudo apt update
```
```
 mkdir arduino
```
```
 cd arduino/
```
```
 wget https://downloads.arduino.cc/arduino-1.8.15-linux64.tar.xz

```
```
 cd arduino-1.8.15/
```
```
 sudo ./install.sh
```





### 2- Install rosserial
```
 sudo apt-get install ros-noetic-rosserial-arduino
```
```
 sudo apt-get install ros-noetic-rosserial
```





### 3- Install ros_lib

go the arduino file and open the terminal 

then type the following commands
```
 cd libraries
```
```
 rosrun rosserial_arduino make_libraries.py
```

***
# Launch RViz
### 7 - launch RViz
```
 roslaunch robot_Arm_pkg check_motors.launch 
```


### 8- Lanuch gazebo
```
 roslaunch robot_Arm_pkg check_motors_gazebo.launch
```
<img width="960" alt="Screenshot 2022-07-26 080258 1240" src="https://user-images.githubusercontent.com/108236308/180927535-8520717c-a882-4e5f-a7e2-eaa43c7b2bf3.png">

***

References : http://wiki.ros.org/rosserial_arduino/Tutorials/Arduino%20IDE%20Setup

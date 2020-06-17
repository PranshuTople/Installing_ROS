# Installing_ROS

Video Tutorial for installing ROS: https://www.youtube.com/watch?v=GBBQqiGvOSw&feature=youtu.be </br>
Full Tutorial Series: https://bit.ly/rostutorials

The below commands are for installing ROS Kinetic Kame on Ubuntu 16.04 </br>
Commands to install other versions of ROS will be updated soon. But you can even try to install those just by replacing ros-kinetic with ros-<your_distro_name> in the given commands. You can click on watch repository icon to know whenever I update the commands.

### Setup sources.list
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```

### Adding Key
```
sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
```

### Update package list
```
sudo apt-get update
```

### Installing ROS Kinetic Full Desktop Version
```
sudo apt-get install ros-kinetic-desktop-full
```

### Initialize Ros Dependencies
```
sudo rosdep init
```
```
rosdep update
```

### Setting up ROS Environment
```
printf "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
```
```
source ~/.bashrc
```

### Installing Python Packages for ROS
```
sudo apt-get install python-rosinstall
```
```
sudo apt install python-catkin-tools
```

### Other Important ROS Packages
```
sudo apt-get install ros-kinetic-tf-*
```
```
sudo apt-get install ros-kinetic-pcl-msgs ros-kinetic-mav-msgs ros-kinetic-mavros ros-kinetic-octomap-* ros-kinetic-geographic-msgs libgeographic-dev
```

### Creating Catkin Workspace
```
mkdir catkin_ws
```
```
cd catkin_ws
```
```
mkdir -p src
```
```
cd src
```
```
catkin_init_workspace
```
```
printf "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc
```
```
cd ~/catkin_ws
```
```
catkin_make
```
```
source ~/catkin_ws/devel/setup.bash
```

### Checking ROS & Gazebo Versions
On Ubunutu 16.04, you should have **ROS Kinetic with Gazebo 7**, </br>
whereas on Ubuntu 18.04, you should have **ROS Melodic with Gazebo 9**
```
rosversion -d
```
```
gazebo -v
```

### Check out ROS Tutorial
http://wiki.ros.org/ROS/Tutorials </br>
Try to complete the Begineer Level tutorials. </br>
If you have any doubts, you can let me know!

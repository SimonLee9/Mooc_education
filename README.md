# Mooc_education
reference : https://emanual.robotis.com/docs/en/platform/turtlebot3/quick-start/

# PC Setup

## Install ROS on Remote PC
$ sudo apt-get update <br />
$ sudo apt-get upgrade <br />
$ wget https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros_kinetic.sh <br />
$ chmod 755 ./install_ros_kinetic.sh <br />
$ bash ./install_ros_kinetic.sh <br />

## Install Dependent ROS Packages
$ sudo apt-get install ros-kinetic-joy ros-kinetic-teleop-twist-joy \
  ros-kinetic-teleop-twist-keyboard ros-kinetic-laser-proc \
  ros-kinetic-rgbd-launch ros-kinetic-depthimage-to-laserscan \
  ros-kinetic-rosserial-arduino ros-kinetic-rosserial-python \
  ros-kinetic-rosserial-server ros-kinetic-rosserial-client \
  ros-kinetic-rosserial-msgs ros-kinetic-amcl ros-kinetic-map-server \
  ros-kinetic-move-base ros-kinetic-urdf ros-kinetic-xacro \
  ros-kinetic-compressed-image-transport ros-kinetic-rqt* \
  ros-kinetic-gmapping ros-kinetic-navigation ros-kinetic-interactive-markers
  
 ## Install TurtleBot3 Packages
$ sudo apt-get install ros-kinetic-dynamixel-sdk <br />
$ sudo apt-get install ros-kinetic-turtlebot3-msgs <br />
$ sudo apt-get install ros-kinetic-turtlebot3 <br />

## Set TurtleBot3 Model Name
$ echo "export TURTLEBOT3_MODEL=burger" >> ~/.bashrc <br />
$ echo "export TURTLEBOT3_MODEL=waffle_pi" >> ~/.bashrc <br />

## Network Configuration
$ ifconfig <br />
$ nano ~/.bashrc <br />
$ source ~/.bashrc <br />

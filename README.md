# Mooc_education
reference : https://emanual.robotis.com/docs/en/platform/turtlebot3/quick-start/

# 1. PC Setup
(reference : https://emanual.robotis.com/docs/en/platform/turtlebot3/quick-start/#pc-setup)
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

# 2. SBC Setup 
(reference : https://emanual.robotis.com/docs/en/platform/turtlebot3/sbc_setup/#sbc-setup)

## Configure the Raspberry Pi
$ ifconfig <br />

$ ssh pi@{IP_ADDRESS_OF_RASPBERRY_PI} <br />

$ sudo apt-get install ntpdate <br />
$ sudo ntpdate ntp.ubuntu.com <br />

$ sudo raspi-config <br />

$ nano ~/.bashrc <br />

export ROS_MASTER_URI=http://{IP_ADDRESS_OF_REMOTE_PC}:11311 <br />
export ROS_HOSTNAME={IP_ADDRESS_OF_RASPBERRY_PI_3} <br />

$ source ~/.bashrc <br />

# 3. OpenCR Setup
(reference : https://emanual.robotis.com/docs/en/platform/turtlebot3/opencr_setup/#opencr-setup)

## OpenCR Setup
$ sudo dpkg --add-architecture armhf <br />
$ sudo apt-get update <br />
$ sudo apt-get install libc6:armhf <br />

$ export OPENCR_PORT=/dev/ttyACM0 <br />
$ export OPENCR_MODEL=burger <br />
$ rm -rf ./opencr_update.tar.bz2 <br />

$ wget https://github.com/ROBOTIS-GIT/OpenCR-Binaries/raw/master/turtlebot3/ROS1/latest/opencr_update.tar.bz2 <br />
$ tar -xvf opencr_update.tar.bz2 <br />

$ cd ./opencr_update <br />
$ ./update.sh $OPENCR_PORT $OPENCR_MODEL.opencr <br />

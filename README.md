# kinetic_sensor_ros
How to use Kinetic sensor in ROS

OS : Ubuntu 16.04 LTS
ROS version : Kinetic
Compiler : catkin

# How to use
1. predependencies

- PCL(Point Cloud Library) Packages 
$ sudo apt-get install ros-kinetic-pcl-conversion

$ sudo apt-get install ros-kinetic-pcl-msgs

$ sudo apt-get install ros-kinetic-pcl-ros 

- sensor_msgs package

$ sudo apt-get install ros-kinetic-sensor-msgs

- roscpp package

$ sudo apt-get install ros-kinetic-roscpp

2. Implement
$ roscore
$ rosrun openni_camera openni_node
$ roslaunch openni_launch openni.launch
$ rosrun chapter4_tutorials my_pcl_tutorial
$ rviz


Fixed Frame을 "camera_depth_frame"으로 변경
Add 버튼을 눌러 PointCloud2를 추가한 후 Topic을 /camera/depth/points로 변경

/camera/depth/points : 기본적으로 Kinetic Sensor에서 뿌려주는 Data

/output : "$ rosrun chapter4_tutorials my_pcl_tutorial" 를 이용해 resolution을 조정한 Data 

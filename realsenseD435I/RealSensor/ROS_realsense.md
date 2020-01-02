# 1. 安装驱动
参照文档安装d435i相关驱动
# 2. 安装ros
版本ubuntu16.04 / ROS kinetic
# 3. 编译ros-realsensor包
```
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/src/
git clone https://github.com/IntelRealSense/realsense-ros.git
cd realsense-ros/
git checkout `git tag | sort -V | grep -P "^\d+\.\d+\.\d+" | tail -1`
cd ..
catkin_init_workspace
cd ..
catkin_make 
source devel/setup.bash

```
# 4. 操作相机node
```
roslaunch realsense2_camera rs_camera.launch
```

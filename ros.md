# ROS noetic
```bash
# To exlude multiple topics from recording in rosbag
rosbag record -a -O data.bag -x "/usb_cam/(.*)|/usb_cam_repub/theora/(.*)"
```
# ROS humble

```bash
# Build the project
mkdir -p ~/ros2_ws/src
cd ~/ros2_ws/src
git clone https://github.com/username/project_name.git
cd ~/ros2_ws
rosdep install --from-paths src --ignore-src -r -y
colcon build --symlink-install
# To source the installed files
source install/setup.bash
```

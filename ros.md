# ROS
```
# To exlude multiple topics from recording in rosbag
rosbag record -a -O data.bag -x "/usb_cam/(.*)|/usb_cam_repub/theora/(.*)"
```

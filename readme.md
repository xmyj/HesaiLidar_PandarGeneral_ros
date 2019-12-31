## How to Launch
0. modify calibration_file and "server_ip" and "lidar_recv_port" in launch file
```
  calibration_file:  vm2.bj.tusimple.ai;download the corresponding "correction.csv" file  to 
  replace the contents of config folder
  servre_ip: vm2.bj.tusimple.ai; check the vehicle.yaml to get lidar_ip and lidar_port to 
  replace the  corresponding content in launch file
```
   
1. While in the `rosworkspace` directory.
```
$ source install/setup.zsh
for Pandar64
$ roslaunch hesai_lidar hesai_lidar.launch

for Pandar40P
$ roslaunch hesai_lidar hesai_lidar.launch lidar_type:="Pandar40P"
```
2. The driver will publish a PointCloud message in the topic.
```
/pandar/points
```
3. Open Rviz and add display by topic.
4. Change fixed frame to `pandar`.

## Some of the available parameters in the Launch file

|Parameter | Default Value|
|---------|---------------|
|lidar_recv_port |2368|
|gps_recv_port  |10110|
|start_angle |0|


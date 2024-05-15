# cob_navi_sim

This package has be created automatically using the [RosTooling](https://github.com/ipa320/RosTooling).


It holds the launch file to run the following nodes:
- joy_node
- teleop_twist_joy_node
- twist_mux
- ros2_laserscan_merger
- pointcloud_to_laserscan
- slam_toolbox
- rviz2
- gazebo
- cob_laserscan
- cob_tricycle_controller
- robot_state_publisher
- cob_joint_state
- amcl
- behavior_server
- bt_navigator
- controller_server
- global_costmap
- lifecycle_manager_localization
- lifecycle_manager_navigation
- local_costmap
- map_server
- planner_server
- smoother_server
- velocity_smoother
- waypoint_follower

The listed nodes offer the following connections:
- Publisher: joy [sensor_msgs/Joy]
- Publisher: cmd_vel [geometry_msgs/Twist]
- Subscriber: cmd_vel [geometry_msgs/Twist]
- Publisher: tricycle_controller/cmd_vel [geometry_msgs/Twist]
- Publisher: cloud_in [sensor_msgs/PointCloud2]
- Subscriber: base_laser_left/scan_raw [sensor_msgs/LaserScan]
- Subscriber: base_laser_right/scan_raw [sensor_msgs/LaserScan]
- Subscriber: base_laser_front/scan_raw [sensor_msgs/LaserScan]
- Subscriber: cloud_in [sensor_msgs/PointCloud2]
- Publisher: scan [sensor_msgs/LaserScan]
- Subscriber: map [nav_msgs/OccupancyGrid]
- Subscriber: scan [sensor_msgs/LaserScan]
- Publisher: map [nav_msgs/OccupancyGrid]
- Publisher: tf [tf2_msgs/TFMessage]
- Subscriber: cloud_in [sensor_msgs/PointCloud2]
- Subscriber: map [nav_msgs/OccupancyGrid]
- Subscriber: robot_description [std_msgs/String]

## Installation

### Using release

This package can be copied to a valid ROS 2 workspace. To be sure that all the related dependencies are intalles the command **rosdep install** can be used.
Then the workspace must be compiled using the common ROS 2 build command:

```
mkdir -p ros2_ws/src
cd ros2_ws/
cp -r PATHtoTHISPackage/cob_navi_sim src/.
rosdep install --from-path src/ -i -y
colcon build
source install/setup.bash
```



## Usage


To execute the launch file, the following command can be called:

```
ros2 launch cob_navi_sim cob_navi_sim.launch.py 
```

The generated launch files requires the xterm package, it can be installed by:

```
sudo apt install xterm
```




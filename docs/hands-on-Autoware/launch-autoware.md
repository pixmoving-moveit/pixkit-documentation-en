# Launching Autoware

Autoware consists of two parts: simulation and real vehicle operation. For simulation, please refer to [Autoware Simulator Tutorials](https://autowarefoundation.github.io/autoware-documentation/main/tutorials/). For real vehicle operation, please refer to the following documentation.

## Launch File and Parameter Configuration

```bash
ros2 launch autoware_launch autoware.launch.xml \
map_path:=$HOME/autoware_map/factory_20230325 \
vehicle_model:=pixkit \
sensor_model:=pixkit_sensor_kit
```

For the above example, this launch is divided into five parts as follows:

- `autoware_launch`: the package where the launch file is located
- `autoware.launch.xml`: the launch file
- `map_path`: the address parameter of the map, which includes the point cloud map and vector map. Please refer to [mapping](../mapping/index.md) for how to create maps.
- `vehicle_model`: the vehicle model parameter. According to the parameter, the corresponding vehicle [URDF model](https://docs.ros.org/en/humble/Tutorials/Intermediate/URDF/URDF-Main.html) and [Autoware interface]((https://github.com/pixmoving-moveit/pix_driver)) will be selected. Please refer to [pixkit_launch](https://github.com/pixmoving-moveit/pixkit_launch).
- `sensor_model`: the sensor model parameter. According to the parameter, the corresponding sensor [URDF model](https://docs.ros.org/en/humble/Tutorials/Intermediate/URDF/URDF-Main.html) and sensor driver will be selected. Please refer to [pixkit_sensor_kit_launch](https://github.com/pixmoving-moveit/pixkit_sensor_kit_launch).

## launch window
After running the above command successfully, the [rviz2](https://github.com/ros2/rviz)window will appear as follows:
![pix](./images/launch.png)
In the visualization window, you can see the imported chassis model, point cloud map, and vector map.

## Launch Verification
- [Verify if the Map is Imported](#verify-if-the-map-is-imported)
- [Verify if the vehicle model is imported](#verify-if-the-vehicle-model-is-imported)
- [Verify whether the sensors have launched correctly](#verify-whether-the-sensors-have-launched-correctly)

### Verify if the Map is Imported
You can check whether the map is imported by:
- Observing whether there is a point cloud map and vector map in rviz.
- Checking whether there is map data published through the [ros2 cli](https://docs.ros.org/en/foxy/Tutorials/Beginner-CLI-Tools.html). If there is data output, it means that the map import is normal. The command is as follows: 
``` bash
ros2 top echo [topic name]
```

| **Topic** | **Type** | **Description** |
|------| ------ | ------ |
| /map/pointcloud_map | sensor_msgs/msg/PointCloud2 | Pointcloud map |
| /map/vector_map | autoware_auto_mapping_msgs/msg/HADMapBin | Vector map (lanelet2 format) |

### Verify if the vehicle model is imported
1. Observe whether there is a vehicle model in the rviz2 visualization window, as shown below:
![vehicle_model](./images/vehicle_model.png)
2. Check whether the chassis feedback is normal. The topics for chassis feedback are shown in the table below. You can check whether the chassis communication is normal through [ros2 cli](https://docs.ros.org/en/foxy/Tutorials/Beginner-CLI-Tools.html). The command is as follows: 
``` bash
ros2 top echo [topic name]
```

| **Topic** | **Type** | **Description** |
| ------ | ------ | ----------- |
| /vehicle/status/control_mode | autoware_auto_vehicle_msgs::msg::ControlModeReport | Feedback on the chassis control mode |
| /vehicle/status/velocity_status | autoware_auto_vehicle_msgs::msg::VelocityReport | Feedback on the chassis velocity |
| /vehicle/status/steering_status | autoware_auto_vehicle_msgs::msg::SteeringReport | Feedback on the chassis steering |
| /vehicle/status/gear_status | autoware_auto_vehicle_msgs::msg::GearReport | Feedback on the chassis gear |
| /vehicle/status/turn_indicators_status | autoware_auto_vehicle_msgs::msg::TurnIndicatorsReport | Feedback on the chassis turn indicators |
| /vehicle/status/hazard_lights_status | autoware_auto_vehicle_msgs::msg::HazardLightsReport | Feedback on the chassis hazard lights |

### Verify whether the sensors have launched correctly
1. Use the [ros2 cli](https://docs.ros.org/en/foxy/Tutorials/Beginner-CLI-Tools.html) to check whether sensor data is being published. If data is being published, it indicates that the sensors have started correctly. The command to check is as follows:
``` bash
ros2 top echo [topic name]
```

| **Topic** | **Type** | **Description** |
| ------ | ------ | ----------- |
| /sensing/lidar/top/outlier_filtered/pointcloud | sensor_msgs/msg/PointCloud2 | LiDAR data |
| /sensing/imu/imu_data | sensor_msgs/msg/Imu | IMU data |


## Notes

- Make sure that the map file exists before launching. Failure to specify a valid folder path or file name in the map_path argument will result in a startup failure.

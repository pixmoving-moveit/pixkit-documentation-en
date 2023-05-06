# Sensor Calibration Introduction

## Overview
In autonomous driving systems, sensor calibration is a critical process that is essential for ensuring the safety and performance of the autonomous driving system. Autonomous driving systems typically require multiple sensors to obtain environmental information around the vehicle, including cameras, LiDARs, and millimeter-wave radars. The calibration of these sensors can help the autonomous driving system accurately perceive and understand the environment around the vehicle.

Specifically, the role of sensor calibration in autonomous driving systems includes:

1. Precise positioning: Through calibration, the position, orientation, and relative distance between different sensors can be accurately determined, thereby achieving more accurate positioning and navigation.
2. Optimized obstacle detection: Calibration can help the autonomous driving system accurately perceive and understand the obstacles around the vehicle, thereby avoiding collisions with other vehicles or objects.
3. Improved lane-keeping ability: Calibration can improve the lane-keeping ability of the autonomous driving system, enabling the vehicle to more accurately recognize and track lanes.
4. Improved prediction ability: Calibration can improve the prediction ability of the autonomous driving system, enabling it to more accurately predict the actions and intentions of other vehicles and pedestrians, thereby improving the safety and driving experience of the vehicle.

## Sensor calibration
- [camera-intrisics-calibration](./camera-intrisics-calibration.md)
- [LiDAR-camera-calibration](./LiDAR-camera-calibration.md)
- [IMU-calibration](./IMU-calibration.md)
- [LiDAR-IMU-calibration](./LiDAR-IMU-calibration.md)
- [LiDAR-LiDAR-calibration](./LiDAR-LiDAR-calibration.md)

## Sensor hardware includes

- LiDAR 
    - [RS-Helios-16P](https://www.robosense.cn/rslidar/RS-Helios)
- Camera
    - [Sensing SG2-OX03CC-5200-GMSL2F-H120](https://www.sensing-world.com/productinfo/913484.html)
- Integrated Navigation
    - [Huace CHC® CGI-410](https://www.huace.cn/product/product_show/467)

## NEXT
Now that you have completed the `Sensor Calibration Introduction`, you can proceed to:

- [Calibration Tool Installation](./calibration_tool_installation.md) 

## References

- [SensorsCalibration](https://github.com/PJLab-ADG/SensorsCalibration)
- [image_pipeline](https://github.com/ros-perception/image_pipeline)
- [calibration_tools](https://github.com/autocore-ai/calibration_tools)
- [camera_calibration](https://navigation.ros.org/tutorials/docs/camera_calibration.html)
- [imu_utils](https://github.com/gaowenliang/imu_utils)
- [code_utils](https://github.com/gaowenliang/code_utils)

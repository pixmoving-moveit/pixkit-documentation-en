# LiDAR LiDAR Calibration

## Overview
## Prerequisites
- Installation of [Calibration Tool](./Installation.md)
- Required hardware:
    - Top LiDAR [RS-Helios-16P]
    - Front bumper LiDAR [RS-Bpearl]
    
## Calibration Procedure
### Step 2: Select Calibration Scene
- There is an elephant-shaped object in front of the vehicle.

### Step 1: Launch Calibration Program

> Observe rviz2, the calibration is complete when the white point cloud and the colored point cloud are completely overlapped.

> - White point cloud: top LiDAR
> - Colored point cloud: front bumper LiDAR

```shell
./calibration_script/lidar2lidar/run_lidar2lidar.sh
```
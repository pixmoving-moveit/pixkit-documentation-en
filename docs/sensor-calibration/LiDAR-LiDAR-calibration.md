# LiDAR LiDAR Calibration

## Overview
## Prerequisites
- Installation of [Calibration Tool](./Installation.md)
- Required hardware:
    - Top LiDAR [RS-Helios-16P]
    - Front bumper LiDAR [RS-Bpearl]
    
## Calibration Procedure
When selecting a calibration site, the following points should be considered:

- The calibration site should be a common viewing area of the two lidars. It should exceed 2m X 2m X 2m and include three-dimensional objects, such as wall corners. This ensures that both lidars observe the same area simultaneously and allows for comparison of their measurements.

### Step 1: Launch Calibration Program

> Observe rviz2, the calibration is complete when the white point cloud and the colored point cloud are completely overlapped.

> - White point cloud: top LiDAR
> - Colored point cloud: front bumper LiDAR

```shell
./calibration_script/lidar2lidar/run_lidar2lidar.sh
```
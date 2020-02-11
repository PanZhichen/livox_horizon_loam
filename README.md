# LOAM-Horizon
## LiDAR Odemetry and Mapping (LOAM) package for Livox Horizon LiDAR

<img src="https://github.com/hku-mars/loam_livox/blob/master/pics/demo_cyt.gif" width = 100% />

**Loam-Horizon** is a robust, low drift, and real time odometry and mapping package for [*Livox LiDARs*](https://www.livoxtech.com/), significant low cost and high performance LiDARs that are designed for massive industrials uses. Our package address many key issues: feature extraction and selection in a very limited FOV, robust outliers rejection, and motion distortion compensation. We use [*Ceres-Solver*](http://ceres-solver.org/) for scan matching to avoid complicated differential geometry derivation. The codes are well structured and streamlined to improve readability and extendability.

In the development of our package, we reference to LOAM, [LOAM_NOTED](https://github.com/cuitaixiang/LOAM_NOTED), and [A-LOAM](https://github.com/HKUST-Aerial-Robotics/A-LOAM).


**Developer:** [Livox](https://www.livoxtech.com)


## 1. Prerequisites
### 1.1 **Ubuntu** and **ROS**
Ubuntu 64-bit 16.04 or 18.04.
ROS Kinetic or Melodic. [ROS Installation](http://wiki.ros.org/ROS/Installation)


### 1.2. **Ceres Solver**
Follow [Ceres Installation](http://ceres-solver.org/installation.html).

### 1.3. **PCL**
Follow [PCL Installation](http://www.pointclouds.org/downloads/linux.html).


## 2. Build
Clone the repository and catkin_make:

```
    cd ~/catkin_ws/src
    git clone https://.../loam_horizon.git
    cd ../
    catkin_make
    source ~/catkin_ws/devel/setup.bash
```
## 3. Directly run
Connect to your PC to Livox LiDAR (horizon) by following  [Livox-ros-driver installation](https://github.com/Livox-SDK/livox_ros_driver), then
```
    ....
    roslaunch loam_horizon loam_livox_horizon.launch
    
```

## 4. Rosbag Example
### 4.1. **Common rosbag**
Download [Our recorded rosbag](,,,) and then
```
roslaunch loam_horizon loam_livox_horizon.launch
rosbag play YOUR_DOWNLOADED.bag
```


### 4.1. **Combined with imu rosbag**

```
roslaunch loam_horizon loam_livox_horizon_imu.launch
rosbag play YOUR_DOWNLOADED.bag
```

## 5.Acknowledgments
Thanks for LOAM(J. Zhang and S. Singh. LOAM: Lidar Odometry and Mapping in Real-time), [LOAM_NOTED](https://github.com/cuitaixiang/LOAM_NOTED), and [A-LOAM](https://github.com/HKUST-Aerial-Robotics/A-LOAM).



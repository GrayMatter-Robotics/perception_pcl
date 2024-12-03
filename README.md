# perception_pcl

[![Build Status](https://travis-ci.org/ros-perception/perception_pcl.svg?branch=melodic-devel)](https://travis-ci.org/ros-perception/perception_pcl)

PCL (Point Cloud Library) ROS interface stack. PCL-ROS is the preferred
bridge for 3D applications involving n-D Point Clouds and 3D geometry
processing in ROS.


## Create Debian Package

Clone the project
```bash
git clone git@github.com:GrayMatter-Robotics/perception_pcl.git
git checkout gmr-dev
```

`pcl_conversions`
```bash
cd pcl_conversions
colcon build

# after the build is done
cd build/pcl_conversions
cpack
```

`pcl_ros`
```bash
cd pcl_ros
colcon build

# after the build is done
cd build/pcl_ros
cpack
```

Upload the artifacts to jfrog.

## Update the ROS Distro

If you want to build the project with different ros distro...

1. Check the release version from [perception_pcl](https://github.com/ros-perception/perception_pcl/releases)
2. Fetch the branch (take humble 2.4.5 for example)
```bash
git remote add upstream git@github.com:ros-perception/perception_pcl.git
git fetch upstream tag 2.4.5
```
3. Apply the changes or rebase against the new branch

### `ply_utils`: ROS 2 utilities for PLY / XYZ / PointCloud2

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT"/></a>
  <a href="https://index.ros.org/p/ply_utils/#jazzy"><img src="https://img.shields.io/ros/v/jazzy/ply_utils" alt="ROS 2 Jazzy version"/></a>
</p>

A single ROS 2 (Jazzy) package bundling three utilities:

- **`pointcloud_to_ply`** — Capture a point cloud from a topic, reconstruct a mesh with PCL, and store it in `.ply` or `.obj` format
- **`ply_to_xyz_transframer`** — Transform a `.ply` file expressed in one frame of reference to a `.xyz` file expressed in another
- **`xyz_to_ply_transframer`** — Transform a `.xyz` file expressed in one frame of reference to a `.ply` file expressed in another

## Build

```bash
cd ~/ros2_ws/src
git clone -b jazzy_devel https://github.com/li9i/ply-utils.git
cd ~/ros2_ws
rosdep install --from-paths src -y --ignore-src
colcon build --packages-select ply_utils
```

## Run

```bash
ros2 launch ply_utils pointcloud_to_ply.launch.xml
ros2 launch ply_utils ply_to_xyz_transframer.launch.xml
ros2 launch ply_utils xyz_to_ply_transframer.launch.xml
```

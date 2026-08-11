# ROS 2 Lyrical + Gazebo Jetty Setup

## System

| Component | Version / Status |
|---|---|
| Ubuntu | 26.04 LTS (Resolute) |
| ROS 2 | Lyrical |
| Gazebo | Gazebo Sim / Jetty |
| Gazebo Sim | 10.4.0 |
| ROS–Gazebo integration | ros-lyrical-ros-gz |
| gz executable | `/opt/ros/lyrical/opt/gz_tools_vendor/bin/gz` |

## Installation Commands

1. Install ROS 2 Lyrical Desktop

```bash
sudo apt update
sudo apt install ros-lyrical-desktop
```

2. Install ROS–Gazebo integration

```bash
sudo apt update
sudo apt install ros-lyrical-ros-gz
```

3. Source ROS 2

For the current terminal:

```bash
source /opt/ros/lyrical/setup.bash
```

To automatically source ROS 2 for new terminals:

```bash
echo "source /opt/ros/lyrical/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

## Verify ROS 2

Run these commands (comments show expected output):

```bash
echo $ROS_DISTRO      # Expected: lyrical
which ros2            # Expected: /opt/ros/lyrical/bin/ros2
ros2 doctor
```

## Verify Gazebo

```bash
which gz              # Expected: /opt/ros/lyrical/opt/gz_tools_vendor/bin/gz
gz sim --version      # Expected: 10.4.0
gz sim                # Launch Gazebo
```

## Current Software Stack

- Ubuntu 26.04 LTS
  - ROS 2 Lyrical
    - ros_gz
  - Gazebo Jetty
    - Gazebo Sim 10.4.0

## Important

Gazebo Sim 10.4.0 is installed and working. Do not install other Gazebo versions (Harmonic, Fortress, Classic) on top of this setup without checking compatibility first.

## Quick Verification

After opening a new terminal, these commands should work:

```bash
echo $ROS_DISTRO
which ros2
ros2 doctor
which gz
gz sim --version
```

Expected important results: `lyrical` and `10.4.0` — this confirms ROS 2 Lyrical and Gazebo Jetty are available in the environment.

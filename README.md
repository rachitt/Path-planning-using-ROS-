
# Path Planning Using ROS

This repository contains the implementation of a **Path Planning** algorithm using **ROS (Robot Operating System)**. It focuses on simulating a robot's ability to navigate through a known environment by avoiding obstacles and finding an optimal path from a start to a goal position.



## Project Overview

This project simulates a robot path-planning scenario using ROS and Gazebo. The robot is tasked with navigating from a start location to a goal location while avoiding obstacles in a 2D grid or a simulated environment. The project demonstrates the implementation of path-planning algorithms, including A* and Dijkstra’s algorithms.

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/rachitt/Path-planning-using-ROS.git
   ```
2. Navigate to the repository:
   ```bash
   cd Path-planning-using-ROS
   ```
3. Build the workspace:
   ```bash
   catkin_make
   source devel/setup.bash
   ```

## Dependencies

Ensure you have the following dependencies installed:
- **ROS Noetic** (Recommended for Ubuntu 20.04)
- **Gazebo** (for simulation)
- **rviz** (for visualization)

Install ROS dependencies using the following:
```bash
sudo apt-get install ros-noetic-navigation ros-noetic-gazebo-ros ros-noetic-ros-control ros-noetic-ros-controllers ros-noetic-rviz
```

## Usage

1. Launch the ROS environment:
   ```bash
   roslaunch path_planning planner.launch
   ```
2. Use `rviz` to visualize the path and robot's progress:
   ```bash
   rosrun rviz rviz
   ```
3. Modify parameters such as the start and goal positions in the `config/planner.yaml` file.

## Nodes Description

- **planner_node**: This node implements the path-planning algorithm (A*/Dijkstra) and publishes the planned path to the robot.
- **controller_node**: Responsible for moving the robot along the planned path while avoiding dynamic obstacles.
- **obstacle_detection_node**: Detects obstacles using simulated sensors and updates the environment map in real-time.

## Contributing

Contributions are welcome! Please fork this repository, create a new branch, and submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

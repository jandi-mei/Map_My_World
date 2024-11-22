# Map My World

## Project Overview
The "Map My World" project involves creating a simulated robot that generates 2D and 3D maps of a given environment using ROS (Robot Operating System) and RTAB-Map (Real-Time Appearance-Based Mapping). The objective of this project is to enable the robot to navigate through a predefined environment, collect sensor data, and create accurate maps while identifying loop closures.

## What Does It Do?
This project allows the robot to:
- Navigate through a simulated environment and gather data using sensors.
- Generate 2D and 3D maps of the environment.
- Identify loop closures to improve mapping accuracy.
- Visualize the mapping process in real-time using RViz.

## Packages and Algorithms Used
- **ROS (Robot Operating System)**: A flexible framework for writing robot software that provides tools and libraries for building robot applications.
- **RTAB-Map (Real-Time Appearance-Based Mapping)**: An algorithm used for simultaneous localization and mapping (SLAM).
- **Gazebo**: A simulation tool that provides a realistic environment for testing robot navigation and mapping.
- **RViz**: A 3D visualization tool for ROS that allows users to visualize the robot's state, sensor data, and generated maps.
- **ROS Navigation Stack**: A collection of software packages that enable navigation capabilities for mobile robots.

## Project Structure
project_directory/ 

    ├── launch/ 
    │ ├── mapping.launch 
    │ ├── teleop.launch 
    │ └── localization.launch 
    ├── maps/ 
    │ └── my_map.yaml 
    ├── world/ 
    │ └── my_world.world 
    └── src/ ├── map_generator.cpp 
    └── robot_control.cpp


## Steps to Run the Project

1. **Install Dependencies**:
   Ensure that you have ROS and Gazebo installed on your system. Follow the installation instructions from the [ROS website](http://wiki.ros.org/ROS/Installation) and the [Gazebo website](http://gazebosim.org/).

2. **Clone the Repository**:
   Clone your project repository to your local machine:
   ```bash
   git clone <repository_url>
   cd project_directory

3. **Build the Project**:
Navigate to the project directory and build the project using catkin_make:

        cd ~/catkin_ws
        catkin_make

4. **Source the Workspace**: Source the workspace to ensure ROS can find your packages:

        source devel/setup.bash

5. **Launch the Gazebo Simulation**:
Launch the world that includes the robot:

        roslaunch world/my_world.launch

6. **Run the Mapping Nodes**:
In a new terminal, run the mapping and localization nodes:

        roslaunch launch/mapping.launch

7. **Visualize in RViz**:
Open RViz to visualize the robot's mapping process and the generated maps:

        rosrun rviz rviz

**Conclusion**
The "Map My World" project demonstrates the integration of mapping algorithms and simulation tools to enable a robot to navigate and understand its environment. This project serves as a practical application of robotics concepts and prepares me for more advanced robotics challenges.

Make sure to replace `<repository_url>` with the actual repo url.

# swarm_robot_ros_sim
A swarm robot simulation environment for ROS to be used with Gazebo.

## Motivation
This project starts after investigating several swarm robot platforms like Kilobot, E-puck, Jasmine, Alice, etc, and working on a novel swarm microrobot called [Inchbot](http://www.case.edu/mae/robotics/#modular) for a while. It would be interesting to see what these swarm microrobots can do as a collective under simulation environment like ROS. This project is also for the purpose of learning programming and various tools in ROS.

## What's inside
*swarm_robot_ros_sim* contains packages each of which features a set of functionalities for this simulation platform:

*swarm_robot_description* package describes the robot models and simulation environment initialization files.

*swarm_robot_msgs* folder contains packages for customized messages, services and actions that will be used in other packages.

*swarm_robot_controller* package contains the low level controllers for the swarm robots.

*swarm_robot_simulation* package contains the swarm algorithms.

## Setup
Have ROS Indigo installed and workspace setup. Clone this package at ~/ros_ws/src and build with catkin_make.

## Demo tests
launch the gazebo environment setting (parameter values are default):
`roslaunch swarm_robot_description initialize.launch robot_name:=two_wheel_robot robot_quantity:=10 robot_range:=1.0`

launch the controllers for two wheel robot:
`roslaunch swarm_robot_controller two_wheel_robot_controller.launch`

test 1: dispersion (parameter values are default):
`rosrun swarm_robot_simulation two_wheel_dispersion _spring_length:=0.7 _wheel_speed:=2.0`

test 2: line formation (parameter values are default)
`rosrun swarm_robot_simulation two_wheel_line_formation _sensing_range:=3.0 _spring_length:=0.7 _wheel_speed:=2.0`

## Why not ROS Stage

## Contribution

## License
See the [LICENSE](LICENSE.md) file for license rights and limitations (MIT).


ackermann_vehicle
=================

ROS packages for simulating a vehicle with Ackermann steering

This fork contains a vehicle with camera and IMU. It also loads a simple track.

## Dependencies
`ros-kinetic-ackermann-msgs`, `ros-kinetic-ackermann-controller`, 
`ros-kinetic-ros-control`, `ros-kinetic-ros-controllers`, 
`ros-kinetic-controller-interface`, `ros-kinetic-controller-manager`, 
`ros-kinetic-controller-manager-msgs`,
`ros-kinetic-gazebo-ros`, `ros-kinetic-gazebo-ros-control`, 
`ros-kinetic-gazebo-msgs`, `ros-kinetic-gazebo-ros-pkgs`,
`ros-kinetic-gazebo-plugins`    

## Usage
`roslaunch ackermann_vehicle_gazebo ackermann_vehicle.launch`

## Controlling the vehicle using ros topics
Highlevel control of the vehicle can be implemented by subscribing to the sensor topics and publishing to the `ackermann_cmd`topic. See [ackermann_controller](https://github.com/alfkjartan/ackermann_controller) for an example. 

## Troubleshooting
The vehicle includes a camera that in some installations of gazebo causes a crash when the gazebo world is launched. These steps install gazebo9 which may help:
1. Remove ros-kinetic-gazebo `sudo apt purge ros-kinetic-gazebo*`
2. Install newer version of gazebo following the instructions for "Alternative installation: Step-by-step" found [here](http://gazebosim.org/tutorials?tut=install_ubuntu). OBS: Instead of installing gazebo in the final step with `sudo apt-get install gazebo9`, install the ros package for gazebo9 using `sudo apt install ros-kinetic-gazebo9-ros ros-kinetic-gazebo9-ros-control ros-kinetic-gazebo9-pkgs ros-kinetic-msgs ros-kinetic-gazebo9-plugins`


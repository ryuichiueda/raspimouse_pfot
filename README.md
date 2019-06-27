# raspimouse_pfot
Package for teach-and-replay of Raspberry Pi Mouse.


## Requirements

This package requires the following to run:
* Robot
  * Raspberry Pi Mouse
* Laser Rangefinder
  * URG-04LX-UG01
* IMU
  * RT-USB-9AXIS-00
* Ubuntu
  * Ubuntu 16.04 (Ubuntu 16.04 Server recomended)
* ROS
  * Kinetic Kame
* ROS Package
  * Customized ROS Navigation Stack - [zaki0929/navigation](https://github.com/zaki0929/navigation)
  * IMU Driver - [AtsushiSaito/lab_usb_9axisimu_driver](https://github.com/AtsushiSaito/lab_usb_9axisimu_driver)
  * urg_node - [urg_node - ROS WiKi](http://wiki.ros.org/urg_node)

## Installation

First of all, install the latest stable version of ROS.
Please refer to [ROS WiKi](http://wiki.ros.org/kinetic/Installation) for installation.

Next, download the dependent ROS package and this repository.

```
sudo apt install ros-kinetic-urg-node
cd ~/catkin_ws/src
git clone https://github.com/zaki0929/navigation.git
git clone https://github.com/AtsushiSaito/lab_usb_9axisimu_driver.git
git clone https://github.com/zaki0929/raspimouse_pfot.git
```

Finally, build the downloaded ones.

```
cd ~/catkin_ws
catkin_make
source ~/catkin_ws/devel/setup.bash
```

## Usage

In order to use this package, you need to launch the launch file on Raspberry Pi Mouse side and PC side as follows.

The map data you want to load is placed in [map](./map).

### Raspberry Pi Mouse side

```
roslaunch raspimouse_pfot remote_robot.launch
```

### PC side

```
roslaunch raspimouse_pfot remote_desktop.launch
```

## License
* This repository is licensed under the MIT license, see [LICENSE](./LICENSE).
* This package is based on zaki0929/raspimouse_navigation_2. 
    * https://github.com/zaki0929/raspimouse_navigation_2

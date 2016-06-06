# Robotiq FANUC Interface

TODO: Write a project description

## Table of Contents

* [Installation](#installation)
* [Usage](#usage)
* [History](#history)
* [Credits](#credits)
* [License](#license)

## <a name="installation"></a>Installation

1. Install [robotiq ROS package](http://wiki.ros.org/robotiq).

  This package provides ROS drivers for the  Robotiq Adaptive Grippers.

2. Install [modbus ROS package](http://wiki.ros.org/modbus).

  This package stack provides a wrapper from the modbus TCP communication to standardized ROS messages

3. Download the [RobotiqFANUCInterface](https://github.com/rarrais/RobotiqFANUCInterface.git) repository to the src folder of your catkin workspace.

  ```bash
  cd ~/catkin_ws/src
  git clone https://github.com/rarrais/RobotiqFANUCInterface.git
  ```
  
4. Build your code. Assuming your catkin workspace is located in ~/catkin_ws:

  ```bash
  cd ~/catkin_ws
  catkin_make
  ```

## <a name="usage"></a> Usage

1. Initialize the **robotiq ROS modbus node**. Make sure to substitute the gripper IP address.

  ```bash
  rosrun robotiq_s_model_control SModelTcpNode.py <gripper_ip_address>
  ```
  
  The default robotic gripper IP address is 192.168.1.11. To connect with this IP address execute the following command:

  ```bash
  rosrun robotiq_s_model_control SModelTcpNode.py 192.168.1.11
  ```

2. Initialize the **robotiq fanuc interface ROS modbus node**. Make sure to substitute the robot IP address.

  ```bash
  rosrun robotiq_fanuc_interface fanuc_interface.py _ip:=<robot_ip_address>
  ```


## <a name="history"></a>History

TODO: Write history

## <a name="credits"></a>Credits

* Developed by [Rafael Arrais](https://github.com/rarrais). 
* Robotiq ROS Package by [Shaun Edwards](https://github.com/shaun-edwards). 
* Modbus ROS Package by [Sven Bock](https://github.com/sven-bock). 

# Robot Operating System Introduction

This repository contains support materials for the UoM-ACM webinar series on Robotics and ROS conducted by Mr. Kalana Ratnayake. A basic introduction to ROS and Robotics can be found in the [Session 1](https://www.youtube.com/watch?v=GO0jsZix18k) of webinar series. Setup Information and terminal-command-snippets required for the robotics webinar series can be found in following sections. 

<br>

## **ROS Installation**

Depending on the Ubuntu Operating system you are using, the setup instructions may vary. Following are the mostly used systems,        

| Ubuntu system | ROS system |  Setup Instructions |
|--------|:-------:|----------------------------------:|
| 20.04  | Noetic  | [link](/Snippets/InstallNoetic.md) |
| 18.04  | Melodic | [link](/Snippets/InstallMelodic.md)|
| 16.04  | Kinetic | [link](/Snippets/InstallKinetic.md)|

<br>

## **ROS Workspace and Packages**

This section ties to the Video [Session 2](https://www.youtube.com/watch?v=GfUcsottFmU) titled Communication infrastructure of ROS (Part-1). Click [here](/Snippets/basicIntro.md) for the instructions and terminal commands which can be directly copy-pasted on to the terminal.

<br>

## **ROS Publisher and Subscriber**

This section ties to the Video [Session 2](https://www.youtube.com/watch?v=GfUcsottFmU) titled Communication infrastructure of ROS (Part-1). This section includes the terminal commands and CMakeLists.txt configuration code snippets used during the session.

Package creation (common for both C++ and Python) - [here](/Snippets/pubsub2package.md)\
C++ based configuration and snippets  -  [here](Snippets/pubsub2cpp.md)\
Python based configuration and snippets - [here](Snippets/pubsub2python.md)

<br>

## **Custom Message Creation and Publisher and Subsciber**

This section ties to the Video [Session 3](https://www.youtube.com/watch?v=ykdC1bTN8NA) titled Communication infrastructure of ROS (Part-1). This section includes the terminal commands and CMakeLists.txt configuration code snippets used during the session.

Package creation (common for both C++ and Python) - [here](/Snippets/pubsub3package.md)\
Custom msg creation and configuration  -  [here](/Snippets/custom_msg.md)\
C++ based configuration and snippets  -  [here](Snippets/pubsub3cpp.md)

<br>

## **ROS Server and Client**

This section ties to the Video [Session 3](https://www.youtube.com/watch?v=ykdC1bTN8NA) titled Communication infrastructure of ROS (Part-2). This section includes the terminal commands and CMakeLists.txt configuration code snippets used during the session.

Package creation (common for both C++ and Python) - [here](/Snippets/cliserverpackage.md)\
Custom srv creation and configuration  -  [here](/Snippets/custom_srv.md)\
C++ based configuration and snippets  -  [here](/Snippets/cliservercpp.md)\
Python based configuration and snippets - [here](/Snippets/cliserverpython.md)

<br>

## **ROS Action Server and Action Client**

This section ties to the Video Session 4 titled Robot Specific Infrastructure. This section includes the terminal commands and CMakeLists.txt configuration code snippets used during the session.

Package creation (common for both C++ and Python) - [here](/Snippets/actionpackage.md)\
Custom action message creation and configuration  -  [here](/Snippets/custom_action.md)\
C++ based configuration and snippets  -  [here](/Snippets/actioncpp.md)\
Python based configuration and snippets - [here](/Snippets/actionpython.md)

<br>

## **ROS Gazebo and Robot Models**

This section ties to the Video Session 4 titled Robot Specific Infrastructure. This section includes the terminal commands and configuration code snippets used during the session.

Package creation  - [here](/Snippets/gazebo_package.md)\
Package operation  - [here](/Snippets/gazebo_package_running.md)
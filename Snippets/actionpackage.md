# Package creation


## Package

Create a package inside src folder

```sh
cd ~/ros_workspace/src
```
```sh
catkin_create_pkg session4_action std_msgs actionlib rospy roscpp
```
```sh
catkin build
```
or you can use following instead "catkin build"
```sh
catkin_make
```
# Package creation


## Package

Create a package inside src folder

```sh
cd ~/ros_workshop/src
```
```sh
catkin_create_pkg session2_pubsub std_msgs rospy roscpp
```
```sh
catkin build
```
or you can use following which comes built-in instead "catkin build"
```sh
catkin_make
```
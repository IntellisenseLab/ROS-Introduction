# Package creation


## Package

Clone the sample package inside src folder

```sh
cd ~/ros_workshop/src
```
```sh
git clone https://github.com/husarion/rosbot_description.git
```

Go to the root and install dependencies
```sh
cd ~/ros_workshop
```

```sh
rosdep install --from-paths src --ignore-src -r -y
```
And build
```sh
catkin build
```
or you can use following instead "catkin build"
```sh
catkin_make
```
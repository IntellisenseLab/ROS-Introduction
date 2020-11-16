# Publisher and Subscriber C++ Implementation

## Publisher modification

Change
```sh
ros::init(argc, argv,"talker");
```
to
```sh
ros::init(argc, argv,"publisher");
```

<br>

## Subscriber modification

Change
```sh
ros::init(argc, argv,"listener");
```
to
```sh
ros::init(argc, argv,"subscriber");
```

<br>

## CMakeLists.txt file modifications

Open session2_pubsub/CMakeLists.txt and add following lines to the bottom of the file.

```sh
add_executable(publisher src/publisher.cpp)
target_link_libraries(publisher ${catkin_LIBRARIES})

add_executable(subscriber src/subscriber.cpp)
target_link_libraries(subscriber ${catkin_LIBRARIES})
```

## Build the code 

Go to root of the workspace

```sh
cd ~/ros_workshop/
```
```sh
catkin build
```
or
```sh
catkin_make
```

## Run the code

Open a terminal and run,

```sh
roscore
```

Open a 2nd terminal in the workspace root and run,
	
```sh
source devel/setup.bash
```
```sh
rosrun session2_pubsub publisher
```

Open a 3rd terminal in the workspace root and run,

```sh
source devel/setup.bash
```
```sh
rosrun session2_pubsub subscriber
```


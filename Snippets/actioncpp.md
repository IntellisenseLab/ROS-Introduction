# Action Server Client C++ Implementation

## CMakeLists.txt file modifications

Open session4_action/CMakeLists.txt and add following lines to the bottom of the file.

```sh
add_executable(ac_server src/ac_server.cpp)
target_link_libraries(ac_server ${catkin_LIBRARIES})
add_dependencies(ac_server ${session4_action_EXPORTED_TARGETS})


add_executable(ac_client src/ac_client.cpp)
target_link_libraries(ac_client ${catkin_LIBRARIES})
add_dependencies(ac_client ${session4_action_EXPORTED_TARGETS})
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
rosrun session4_action ac_server
```

Open a 3rd terminal in the workspace root and run,

```sh
source devel/setup.bash
```
```sh
rosrun session4_action ac_client
```


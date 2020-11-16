# Client Server C++ Implementation

## CMakeLists.txt file modifications

Open session3_cliserver/CMakeLists.txt and add following lines to the bottom of the file.

```sh
add_executable(server src/server.cpp)
target_link_libraries(server ${catkin_LIBRARIES})
add_dependencies(server session3_cliserver_generate_messages_cpp)


add_executable(client src/client.cpp)
target_link_libraries(client ${catkin_LIBRARIES})
add_dependencies(client session3_cliserver_generate_messages_cpp)
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
rosrun session3_cliserver server
```

Open a 3rd terminal in the workspace root and run,

```sh
source devel/setup.bash
```
```sh
rosrun session3_cliserver client
```


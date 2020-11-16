# Custom Message Creation and Publisher and Subsciber

## Messages

Create a srv folder inside session3_cliserver folder

```sh
mkdir -p ~/ros_workspace/src/session3_cliserver/srv
```

Open the folder 
```sh
cd ~/ros_workspace/src/session3_cliserver/srv
```

Create a .srv file with desired name. (we will select custom.srv as an example)

```sh
code custom.srv
```
Inside the file add following lines, then save and close.
```sh
uint8 a
uint8 b
---
uint16 result
```

Open package.xml and add the following lines in the respective sections

```sh
<build_depend>message_generation</build_depend>
<exec_depend>message_runtime</exec_depend>
```

Open the CMakeLists.txt and add following lines to respective section,

message_generation to find_package()

```sh
find_package(catkin REQUIRED COMPONENTS
   roscpp
   rospy
   std_msgs
   message_generation
)
```

message_runtime to catkin_package

```sh
catkin_package(
  ...
  CATKIN_DEPENDS message_runtime ...
  ...)
```

uncomment add_service_files section and add custom.srv file

```sh
add_service_files(DIRECTORY 
  srv
  FILES
  custom.srv
)
```

uncomment generate_messgae() section. It shoul look like this,

```sh
generate_messages(
  DEPENDENCIES
  std_msgs
)
```

Move to the workspace root and rebuild

```sh
cd ~/ros_workspace/
```
```sh
catkin build
```
or
```sh
catkin_make
```
# Custom Message Creation

## Messages

Create a msg folder inside session3_pubsub folder

```sh
mkdir -p ~/ros_workshop/src/session3_pubsub/msg
```

Open the folder 
```sh
cd ~/ros_workshop/src/session3_pubsub/msg
```

Create a .msg file with desired name. (we will select custom.msg as an example)

```sh
code custom.msg
```
Inside the file add following lines, then save and close.
```sh
string first_name
string last_name
uint8 age
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

uncomment add_message_files section and add custom.msg file

```sh
add_message_files(DIRECTORY 
  msg
  FILES
  custom.msg
)
```

uncomment generate_messgae() section. It shoul look like this,

```sh
generate_messages(
  DEPENDENCIES
  std_msgs
)
```

Move to the root of workspace and rebuild

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


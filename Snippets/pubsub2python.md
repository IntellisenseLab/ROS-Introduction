# Publisher and Subscriber C++ Implementation

Create a folder name scripts inside src folder

```sh
mkdir scripts
```

## Publisher modification

Change
```sh
rospy.init_node('talker', anonymous=True)
```
to
```sh
rospy.init_node('publisher', anonymous=True)
```
Open a terminal in the file location and Run

```sh
chmod +x publisher.py
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
and open a terminal in the file location and Run,

```sh
chmod +x subscriber.py
```
<br>

## CMakeLists.txt file modifications

Open session2_pubsub/CMakeLists.txt and add following lines to the bottom of the file.

```sh
catkin_install_python(PROGRAMS scripts/subscriber.py scripts/publisher.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

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
rosrun session2_pubsub publisher.py
```

Open a 3rd terminal in the workspace root and run,

```sh
source devel/setup.bash
```
```sh
rosrun session2_pubsub subscriber.py
```
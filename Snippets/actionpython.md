# Action Server Client Python Implementation

```sh
mkdir scripts
```

## Sever modification

Open a terminal in the file location and Run

```sh
chmod +x ac_server.py
```

<br>

## Client modification

Open a terminal in the file location and Run,

```sh
chmod +x ac_client.py
```
<br>

## CMakeLists.txt file modifications

Open session4_action/CMakeLists.txt and add following lines to the bottom of the file.

```sh
catkin_install_python(PROGRAMS scripts/ac_client.py scripts/ac_server.py
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
rosrun session4_action ac_server.py
```

Open a 3rd terminal in the workspace root and run,

```sh
source devel/setup.bash
```
```sh
rosrun session4_action ac_client.py
```
# Client Server Python Implementation

```sh
mkdir scripts
```

## Server modification

Open a terminal in the file location and Run

```sh
chmod +x server.py
```

<br>

## Client modification

Open a terminal in the file location and Run,

```sh
chmod +x client.py
```
<br>

## CMakeLists.txt file modifications

Open session3_cliserver/CMakeLists.txt and add following lines to the bottom of the file.

```sh
catkin_install_python(PROGRAMS scripts/client.py scripts/server.py
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
rosrun session3_cliserver server.py
```

Open a 3rd terminal in the workspace root and run,

```sh
source devel/setup.bash
```
```sh
rosrun session3_cliserver client.py
```
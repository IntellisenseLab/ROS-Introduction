# Basic Initialization into any ROS porject

## Workspace

To create the workspace folder and do the initial setup,

```sh
mkdir -p ~/<workspace_name>/src
```
As an example (we will be using this workspace from here on),

```sh
mkdir -p ~/ros_workspace/src
```

Enter the workspace and build it.

```sh
cd ~/ros_workspace/
```
```sh
catkin build
```

<br>
<br>

## Package

To create a package

```sh
cd ~/ros_workspace/src
```
```sh
catkin_create_pkg <package_name> [depend1] [depend2] [depend3]
```

As an example,

```sh
catkin_create_pkg session2_tutorials std_msgs rospy roscpp
```

To build the package,

```sh
catkin build
```

<br>

**Note** : Catkin build command gives a abstract view of the build process or incase it does not work,

```sh
catkin_make
```

command can be used. It comes as an inbuilt tool with ROS and gives a detailed output on the build process.

<br>
<br>

## Initialization

To setup new environment variables,

```sh
source devel/setup.bash
```

<br>

### We will be using the workspace created here but will create new packages for each component
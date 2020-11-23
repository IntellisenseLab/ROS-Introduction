# RQT_TF_TREE

## Simulation

Start the world

```sh
source devel/setup.bash
```
```sh
roslaunch rosbot_gazebo rosbot_world.launch
```

Add the rosbot model
```sh
source devel/setup.bash
```

```sh
roslaunch rosbot_description rosbot_gazebo.launch
```
Start the key operation
```sh
source devel/setup.bash
```
```sh
roslaunch rosbot_navigation rosbot_teleop.launch
```

<br>

## Start rqt_tf_tree

In a seperate terminal

```sh
rosrun rqt_tf_tree rqt_tf_tree
```
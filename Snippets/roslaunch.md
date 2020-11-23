# ROSLAUNCH


## Syntax

```sh
<node pkg=<package name> type=<node name> name=<node visible name> output=<type> />
```

<br>

## Sample launch file

```sh

<launch>
    <node pkg="session3_pubsub" type="publisher" name="publisher_1" output="screen" />
    <node pkg="session3_pubsub" type="publisher" name="publisher_2" output="screen" />
    <node pkg="session3_pubsub" type="subscriber" name="subscriber" output="screen" />
</launch>

```

## Use

Open a terminal and run,
	
```sh
source devel/setup.bash
```
```sh
roslaunch session3_pubsub test.launch
```

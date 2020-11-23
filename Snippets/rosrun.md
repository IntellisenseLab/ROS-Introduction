# ROSRUN


## Basic Use

Open a terminal and run,

```sh
roscore
```

Open a 2nd terminal in the workspace root and run,
	
```sh
source devel/setup.bash
```
```sh
rosrun session3_pubsub publisher
```

Open a 3rd terminal in the workspace root and run,

```sh
source devel/setup.bash
```
```sh
rosrun session3_pubsub subscriber
```

Open a 4th terminal in the workspace root and run,

```sh
source devel/setup.bash
```
```sh
rosrun session3_pubsub publisher
```

<br>

## With renaming

Open a terminal and run,

```sh
roscore
```

Open a 2nd terminal in the workspace root and run,
	
```sh
source devel/setup.bash
```
```sh
rosrun session3_pubsub publisher __name:=publisher1
```

Open a 3rd terminal in the workspace root and run,

```sh
source devel/setup.bash
```
```sh
rosrun session3_pubsub subscriber
```

Open a 4th terminal in the workspace root and run,

```sh
source devel/setup.bash
```
```sh
rosrun session3_pubsub publisher __name:=publisher2  
```
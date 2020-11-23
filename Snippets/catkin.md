# Catkin build system


Basic command

```sh
catkin_make
```

Basic command multi threaded
```sh
catkin_make -j 4
```


<br>

Command when there are non ros packages/libraries

```sh
catkin_make_isolated
```

Multi threaded command when there are non ros packages/libraries

```sh
catkin_make_isolated -j 4
```

<br>


Abstract command

```sh
catkin build
```
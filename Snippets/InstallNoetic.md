# ROS Noetic Installation (for Ubuntu 20.04)

Setup your computer to accept ROS related software

```sh
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```

Then setup keys

```sh
sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
```

To install ROS, 

```sh
sudo apt update
```

```sh
sudo apt install ros-noetic-desktop-full
```

Setup environment

```sh
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
```

```sh
source ~/.bashrc
```

Dependencies

```sh
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```

```sh
sudo rosdep init
```

```sh
rosdep update
```

To setup catkin tools
```sh
sudo apt-get install python3-catkin-tools
```


Setup VS code as text editor
https://linuxize.com/post/how-to-install-visual-studio-code-on-ubuntu-20-04/

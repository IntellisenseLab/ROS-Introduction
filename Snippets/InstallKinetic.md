# ROS Kinetic Installation (for Ubuntu 16.04)

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
sudo apt-get install ros-kinetic-desktop-full
```

Setup environment

```sh
echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
```

```sh
source ~/.bashrc
```

Dependencies

```sh
sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential
```

```sh
sudo rosdep init
```

```sh
rosdep update
```

To setup catkin tools
```sh
sudo apt-get install python-catkin-tools
```


Setup VS code as text editor

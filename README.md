# Turtle Pong

This repository hosts the source code for the ROS `turtle_pong` package which 
implements the Pong arcade video game for the Robot Operating System (ROS 1 Noetic) using turtlesim.

![Short Game Play](docs/turtle_pong.gif)

To learn how the package was created, please read the [documentation](https://fjp.at/ros/turtle-pong).

## Usage

To use the `turtle_pong` package clone this repository into the `src` folder of your catkin workspace, then build the workspace with `catkin_make` and source the new package:

```console
cd ~/catkin_ws/src
git clone https://github.com/Jakubach/ros-turtle-pong.git
cd ~/catkin_ws
catkin_make
source devel/setup.bash
```

Finally start `roscore`, run `turtlesim` and `pong.launch`:

```console
roscore
rosrun turtlesim turtlesim_node
roslaunch turtle_pong pong.launch
```

Note that each of the three commands above should be executed from another terminal so that it will run in its own process.

You can use one launch file instead of running these commands separately:

```console
roslaunch turtle_pong pong_single_launch.launch
```

The game can be played with the w/s keys and the up/down arrow keys to control the left and right player (turtle) respectively.

## ROS Node Graph

![rqt node graph](docs/rosgraph.svg)


## Current Version and Missing Features

This is the first release (version 0.0.0). The following features are planned and contributions to them or new features and code improvements are welcome.

- Handle missed ball cases (left and right)
- Add score board logic (for example using new turtle to draw player scores)
- Fix bounce angle logic when ball hit a paddle.
- Add AI Player
- Improve keyboard input
- Fix order of node launches
- ...

The short video below gives more insights on what is currently implemented:

[![Turtle Pong YouTube](http://img.youtube.com/vi/i83dNyfm_QE/0.jpg)](https://youtu.be/i83dNyfm_QE)

# ROS-2-Turtlesim-Keyboard-Teleoperation-Demo
This project demonstrates a basic ROS 2 setup using the `turtlesim` package with keyboard teleoperation and action feedback visualization. It includes launching the simulator, controlling the turtle with the keyboard, and visualizing the node/topic graph using `rqt_graph`.
---

## Requirements

- Ubuntu 22.04
- ROS 2 Humble Hawksbill
- `turtlesim` package (pre-installed with ROS 2)
- `rqt_graph` for graph visualization

---

##  How to Run

1. **Launch the Turtlesim Node**

```bash
ros2 run turtlesim turtlesim_node
```


2. **Launch the Teleoperation Node**

Open a new terminal and run:

```bash
ros2 run turtlesim turtle_teleop_key
```


3. **Control the Turtle**

Use your keyboard:

Arrow keys → move turtle

G|B|V|C|D|E|R|T → rotate to absolute orientations

F → cancel rotation

Q → quit
Visualize the ROS Graph


4. **Visualize the ROS Graph**
 In a third terminal:

```bash
rqt_graph
```
---

## ROS 2 Graph Overview
<img width="1041" height="186" alt="Image" src="https://github.com/user-attachments/assets/dce87602-2642-4ae7-badb-120200fdb165" />
**Nodes**

/turtlesim: Runs the turtlesim simulator

/teleop_turtle: Listens to keyboard input and publishes velocity commands

**Topics**

/turtle1/cmd_vel: Published by /teleop_turtle, subscribed by /turtlesim

/turtle1/rotate_absolute/_action/feedback: Action feedback topic

/turtle1/rotate_absolute/_action/status: Action status topic

---

## Screenshots
Turtlesim Running and Teleop Control




نسخ
تحرير

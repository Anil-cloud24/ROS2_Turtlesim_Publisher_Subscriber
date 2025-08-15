# ROS 2 Publisher & Subscriber with Turtlesim

This project demonstrates creating a **ROS 2 publisher** to control the movement of a turtle in the `turtlesim` simulator, and a **subscriber** to listen to the turtle's motion commands.  
It uses **Python** and the ROS 2 client library `rclpy`.

---

## 📌 Project Overview

- **Publisher (`publisher_pkg`)**: Publishes `geometry_msgs/Twist` messages to `/turtle1/cmd_vel` to control the turtle’s movement.
- **Subscriber (`subscriber_pkg`)**: Subscribes to `/turtle1/cmd_vel` and logs the received motion commands.
- **Turtlesim**: A lightweight ROS simulator for learning and testing publisher/subscriber concepts.

---

## 🛠 Prerequisites

- **ROS 2** installed (tested with Humble/Foxy)
- **Python 3**
- `turtlesim` package
  
---

## 📂 Project Structure

```text
ros2_ws/
├── src/
│   ├── publisher_pkg/
│   │   ├── publisher_pkg/simple_publisher.py
│   │   ├── launch/publisher_pkg_launch_file.launch.py
│   │   ├── setup.py
│   │   └── package.xml
│   ├── subscriber_pkg/
│   │   ├── subscriber_pkg/subscription.py
│   │   ├── launch/sub_launch_file.launch.py
│   │   ├── setup.py
│   │   └── package.xml
```

---

## 🚀 How to Run

### 1 Open Turtlesim
ros2 run turtlesim turtlesim_node

### 2 Build the Workspace
cd ~/ros2_ws
colcon build
source install/setup.bash

### 3 Run the Publisher
ros2 launch publisher_pkg publisher_pkg_launch_file.launch.py

### 4 Run the Subscriber
ros2 launch subscriber_pkg sub_launch_file.launch.py

The subscriber will log the velocity commands received from the publisher.

---

## 📦 Launch Files
- Publisher Launch → publisher_pkg/launch/publisher_pkg_launch_file.launch.py
- Subscriber Launch → subscriber_pkg/launch/sub_launch_file.launch.py

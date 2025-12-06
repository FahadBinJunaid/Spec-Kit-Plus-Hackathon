# Chapter 2 — ROS 2: The Robotic Nervous System

In humanoid robotics, **ROS 2 (Robot Operating System 2)** functions as the robot's nervous system.  
It enables communication between sensors, processors, and actuators in real-time, forming the foundation for any intelligent physical AI system.

---

## 🌐 What is ROS 2?

ROS 2 is an open-source **middleware** framework designed for robotic software development.  
It provides a standardized way to:

- Communicate between components (nodes)  
- Stream data reliably  
- Execute commands asynchronously  
- Integrate AI and sensor systems seamlessly  

ROS 2 is essential for building scalable and modular robotic applications.

---

## 🧩 Core Concepts

### 1. Nodes
Nodes are the smallest executable units in ROS 2. Each node performs a single task, such as reading sensor data or controlling a motor.

**Example nodes**:

- `camera_node`: Captures RGB and depth data from a camera  
- `lidar_node`: Streams distance readings from a LiDAR  
- `navigation_node`: Calculates paths and coordinates movements  
- `arm_controller_node`: Controls robotic arm joints  

Nodes can communicate across the network or even different machines.

---

### 2. Topics
Topics are **publish/subscribe channels** for streaming data asynchronously.  

**Examples**:

| Topic               | Type                | Purpose |
|--------------------|------------------|---------|
| `/camera/image_raw` | `sensor_msgs/Image` | Camera feed for perception |
| `/lidar/scan`      | `sensor_msgs/LaserScan` | Distance measurements from LiDAR |
| `/joint_states`    | `sensor_msgs/JointState` | Current angles of all joints |

Nodes **publish** or **subscribe** to topics without needing to know about other nodes directly.  
This makes ROS 2 extremely modular.

---

### 3. Services
Services are **synchronous request-response mechanisms**.  
They are used for tasks that require a specific result immediately.

**Example: Reset robot odometry**  

```bash
ros2 service call /reset_odometry std_srvs/srv/Empty
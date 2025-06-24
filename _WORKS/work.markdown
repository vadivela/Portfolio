---
title: Color Cube Sorting Robotic Arm
description: Developed a 4-DOF robotic arm system capable of detecting and sorting colored cubes on a conveyor using real-time sensors and multiprocessing control logic. Designed for efficient, autonomous material handling in structured environments.

imgurl: work3.gif
---

# **Project Overview**
This project showcases an autonomous 4-DOF robotic arm designed to identify and sort colored cubes on a conveyor belt. The system uses a color sensor and an ultrasonic sensor to detect object attributes in real time, allowing the robot to accurately position and drop the cubes into designated bins based on color.

---

# **Key Features**
- **Real-Time Color Detection**:  
  Used a color sensor to classify cube colors (e.g., red, blue, green) while moving on a conveyor.

- **Distance-Based Triggering**:  
  An ultrasonic sensor measured proximity, ensuring the arm activated only when an object was within range.

- **Efficient Sorting Algorithm**:  
  Implemented multiprocessing on a Parallax Propeller Board to simultaneously read color and distance inputs, ensuring rapid and synchronized sorting actions.

---

# **Technical Breakdown**

### 1. **Hardware Design**
- Built a 4-DOF robotic arm with a custom gripper for object pick-and-drop.
- Integrated the arm with a conveyor system for continuous sorting.

### 2. **Sensor Integration**
- Calibrated a TCS34725 color sensor for reliable cube color detection.
- Positioned an ultrasonic sensor to detect when a cube enters the pickup zone.

### 3. **Multiprocessing Control**
- Utilized Parallax Propeller’s multiple cores to handle color reading and arm control in parallel.
- Ensured minimal latency between object detection and sorting actions.

---

# **Applications**
- **Smart Warehousing**: Automates small-scale item sorting in controlled logistics.
- **STEM Education**: Demonstrates concepts of sensor fusion, robotic kinematics, and embedded logic.
- **Prototyping**: Foundation for scalable conveyor-based automation systems.

---

[🔗 View Source Code on GitHub](https://github.com/vadivela/Color-Cube-Sorting-Robotic-Arm)

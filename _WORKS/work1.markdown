---
title: Autonomous Mobile Robot for Color-Based Object Retrieval
description: Designed and developed a mobile robot capable of autonomously detecting, navigating to, and retrieving colored cubes in a controlled environment. This project combined computer vision, object localization, and motion control to execute reliable pick-and-place operations based on color recognition.

imgurl: work1.gif
---

# **Highlights**:
- **Camera Calibration**: Mapped 2D image coordinates to 3D spatial positions using intrinsic and extrinsic camera properties.
- **Vision-Based Detection**: Identified object color and shape with high precision under varying conditions.
- **Real-World Localization**: Determined both object and robot positioning within a known reference frame.
- **PID-Controlled Motion**: Smooth and accurate robot movement using feedback-based trajectory correction.

---

# **Technical Workflow**:

### **1. Camera Calibration**
**Goal**: Establish a relationship between image pixels and real-world coordinates.  
- **Intrinsic Calibration**: Obtained using 30 checkerboard image sets in MATLAB to derive focal length, principal point, and lens distortion.
- **Extrinsic Calibration**: Used known corner positions of the arena to determine the camera's position and orientation relative to the environment.

---

### **2. Color and Shape Recognition**
1. Captured frames processed in real time.
2. Converted color space from BGR to HSV for more effective segmentation.
3. Applied color masks to isolate target hues (blue, green, magenta).
4. Calculated centroids using image moments.
5. Differentiated cubes from patches based on contour area.
6. Transformed detected centroid coordinates to world space.

---

### **3. Object and Robot Localization**
Using the derived calibration parameters, both the robot’s and object’s global positions were calculated.  
- **Depth Calculation**: Depth (`Z_w`) was computed first, followed by lateral (`X_w`, `Y_w`) world coordinates.

---

### **4. Autonomous Navigation**
**Control Strategy**:  
- A PID controller regulated wheel velocities to direct the robot toward the target.  
- Navigation relied on minimizing orientation error between the robot and the goal point.

**Tuning Details**:
- Initially modeled in Simulink for parameter estimation:  
  - `Kp` = 1.317, `Ki` = 0.5039, `Kd` = -0.1388  
- Final values adjusted manually based on field performance:  
  - `Kp` = 1, `Ki` = 0, `Kd` = 0

---

# **Real-World Applications**:
- **Warehouse Automation**: Efficient retrieval and sorting systems.
- **Manufacturing**: Automated material handling solutions.
- **Research Platforms**: Prototyping intelligent robotic behaviors.


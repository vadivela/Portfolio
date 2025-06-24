---
title: Teleoperated 4-DOF Robotic Arm
description: Built a fully functional 4-DOF robotic arm controlled via a puppet model with potentiometers. Enabled intuitive teleoperation, pose recording, and real-time mirror functionality—simulating industrial pick-and-place applications.

imgurl: work2.gif
---

# **Project Overview**
This project features a teleoperated robotic arm system where a custom-built puppet model is used to intuitively control the movement of a 4-DOF robotic arm. Designed for real-time mirroring, it allows users to teach positions and automate sequences, making it ideal for education and prototyping.

---

# **Key Features**
- **Puppet-Based Control Interface**:  
  A physical puppet equipped with potentiometers was used to manipulate the arm joints in real-time, enabling intuitive and direct control.

- **Programmable Positioning**:  
  Implemented memory functionality to store and retrieve up to 10 unique positions, allowing the arm to cycle through pre-taught motions.

- **Mirror Mode Operation**:  
  Enabled live synchronization between the puppet and robotic arm, providing immediate feedback and realistic joint replication.

---

# **Technical Breakdown**

### 1. **Hardware Architecture**
- Designed and assembled a 4-DOF robotic arm using servo motors.
- Created a puppet rig with one potentiometer per joint, mimicking real-world articulation.

### 2. **Control Logic**
- Used analog-to-digital conversion to read voltages from the puppet model.
- Translated voltage inputs into precise joint angles and sent them to servos via microcontroller logic.

### 3. **Pose Recording System**
- Added push-button controls to record and cycle through multiple saved configurations.
- Created a seamless interface for position teaching and repetitive automation tasks.

---

# **Applications**
- **Educational Labs**: Demonstrates kinematics and control in an interactive format.
- **Teleoperation Research**: Forms a foundation for exploring remote and assistive manipulation.
- **Industrial Prototyping**: Simulates task automation for low-cost experimentation.

---

[🔗 View Source Code on GitHub](https://github.com/vadivela/Teleoperation-of-Robotic-ARM)

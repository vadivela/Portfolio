---
title: Proactive Human-Manipulator Collision Avoidance
description: Developed a real-time, predictive motion planning system for the UR16e robotic arm using 3D human pose estimation, motion forecasting, APF-based safety evaluation, and GPU-accelerated A-RRT* trajectory replanning in a ROS 2-based digital twin.

imgurl: work.gif
---

# **Project Overview**
This project implements a human-aware motion planning framework for the UR16e robotic manipulator to operate safely in dynamic, shared environments. By combining real-time 3D pose tracking, neural motion prediction, and adaptive trajectory generation, the robot proactively avoids collisions with human operators—anticipating their future movements and adjusting its path before conflict occurs.

The system is fully integrated in a ROS 2 digital twin, simulating both the robot and human in Gazebo and RViz with live replanning using GPU-accelerated algorithms.

---

# **Key Components**

- **3D Human Pose Estimation**:  
  Extracted real-time skeletal joints using the Orbbec Femto Bolt depth camera and MediaPipe.

- **Motion Forecasting (LSTM Model)**:  
  Predicted short-term human motion using a Bi-LSTM neural network trained on normalized joint sequences.

- **Artificial Potential Field (APF) Evaluation**:  
  Quantified collision risk between predicted human skeleton and robot links using a capsule model.

- **Adaptive RRT***:  
  Implemented a GPU-accelerated A-RRT* planner using CuPy for rapid trajectory generation in response to predicted motion.

- **Digital Twin Environment**:  
  Simulated the UR16e robot and human in Gazebo, with RViz visualizations of current and future human joint positions.

- **Real-Time Control Execution**:  
  Sent planned joint trajectories to the UR16e via ROS 2 controllers, with dynamic halting and replanning logic based on APF thresholds.

---

# **Performance Highlights**

- Achieved real-time replanning speeds of **0.6–2.0 seconds**
- Maintained minimum robot-human clearance of **≥ 275 mm**
- Triggered safe trajectory replans in **100% of unsafe scenarios**
- End-to-end latency (prediction to actuation) under **200 ms**

---

# **Applications**

- **Collaborative Robotics**: Enhancing safety in shared industrial workspaces.
- **Smart Manufacturing**: Human-in-the-loop automation with predictive motion planning.
- **Research & Prototyping**: Testing safe HRI strategies in digital twin environments before physical deployment.

---

[🔗 View Full Code on GitHub](https://github.com/vadivela/Proactive-Human-Manipulator-collision-avoidance-through-motion-prediction-and-ROS)
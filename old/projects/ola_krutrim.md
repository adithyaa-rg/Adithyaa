---
title: "ADAS Planning Pipeline — Ola Krutrim"
layout: default
---

## Ola Krutrim — Computer Vision & Planning Engineer

<img src="images/ola_krutrim_logo.png" alt="Ola Krutrim" style="width:160px; border:none; background:transparent; margin:0.5rem 0 1.5rem;">

**Role:** Computer Vision & Planning Engineer Intern  
**Team:** Embodied AI  
**Duration:** May – July 2025 (Completed)

---

### Overview

I worked within the Embodied AI team at Ola Krutrim to develop an end-to-end planning and control pipeline for a 4-wheeled ADAS (Advanced Driver-Assistance System) platform. The goal was to enable autonomous navigation over challenging terrains and real Indian road conditions.

---

### Planning & Control Stack

The system was built on **ROS2 and the Nav2 navigation stack**:

- **Global Planner:** SMAC Planner for high-level path planning over occupancy grids
- **Local Controller:** MPPI (Model Predictive Path Integral) Controller for real-time reactive control, handling dynamic obstacles and uneven terrain
- **Simulation:** NVIDIA Isaac Sim was used for system evaluation in a high-fidelity physics environment before on-ground testing
- **On-Ground Validation:** Deployed and tested on a Honda City, tracking pre-defined trajectories and conducting live on-road tests

---

### LIDAR-Camera Fusion

A significant part of the internship involved building a **five-camera LIDAR-camera fusion pipeline** for local environment perception:

- Fused depth information from a spinning LIDAR with images from five cameras covering a 360° field of view
- Generated costmaps from the fused data for consumption by the MPPI local planner
- Handled extrinsic calibration, temporal synchronisation, and projection of LIDAR points into camera frames

---

### Key Learnings

Working at the intersection of simulation and hardware taught me how significant the sim-to-real gap can be — and how to design pipelines that are robust to it. Validating the system on an actual Honda City on Mumbai roads was a highlight of the experience.

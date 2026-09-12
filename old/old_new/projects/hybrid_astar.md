---
title: "Greedy Multi-Agent Hybrid A*"
layout: default
---

## Greedy Multi-Agent Hybrid A* Path Planning

**Course:** Multi-Agent Systems & AI (DD2438) — KTH Royal Institute of Technology  
**Advisor:** Prof. Petter Ögren  
**Duration:** February – March 2025 · Stockholm, Sweden  
**Result:** 🏆 3rd Place in Class Competition

---

### Problem

Plan collision-free paths for multiple heterogeneous agents (cars and drones) to reach multiple targets in a shared environment — minimising total mission time while ensuring smooth, physically realisable trajectories.

---

### Hybrid A*

Standard A* plans on a discrete grid, which produces jerky paths that cars and drones cannot follow due to kinodynamic constraints (turning radius, minimum speed, etc.). **Hybrid A*** extends A* to a continuous 3D state space `(x, y, θ)`, generating paths that respect vehicle kinematics.

---

### Our Contributions

**Greedy Prioritised Planning**  
Rather than solving the joint multi-agent problem (which is exponentially hard), we used a **greedy prioritisation scheme**: agents are ordered by urgency, and each plans its path while treating previously planned paths as dynamic obstacles. This gives near-optimal results in practice at a fraction of the computational cost.

**Forward-Backward Velocity Profiling**  
Given a geometric path from Hybrid A*, we compute a smooth velocity profile using a forward-backward pass over path curvature:
- Forward pass: accelerate from rest, respecting curvature-constrained max speed
- Backward pass: ensure the agent can decelerate in time for tight corners and stopping points

This produces time-optimal velocity profiles that are smooth and physically achievable.

**PID Trajectory Tracking**  
At execution time, a PID controller handles real-time trajectory tracking for both car and drone agents. Separate gains were tuned for each vehicle type; the controller handles cross-track error and heading error simultaneously.

---

### Results

The system consistently completed multi-target missions in minimum time. Placed **3rd out of the full cohort** in the live class competition, with particularly strong performance on environments with narrow corridors requiring precise velocity management.

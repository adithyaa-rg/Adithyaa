---
title: "Human Takeover Steering System"
layout: default
---

## User Study for Human Takeover Steering System

**Advisor:** [Prof. Bijo Sebastian](https://ed.iitm.ac.in/~bijo/), Autonomous Systems Lab, IIT Madras  
**Collaborators:** V Bagaria  
**Duration:** July 2024 – January 2025 (Paper Accepted)

---

### Problem

When an autonomous vehicle encounters a scenario it cannot handle, it must seamlessly transfer control to the human driver. This *control handover* is a critical safety moment — sudden or jarring transitions can disorient drivers and cause accidents. How should the handover feel? How much haptic feedback is too much? How quickly can a human take over?

These are the questions this project set out to answer.

---

### Hardware System

I designed and built a custom interactive steering system around the **CubeMars AK-80 quasi-direct-drive motor** — a high-torque, low-inertia actuator capable of precise torque and position control:

- **Autonomous Mode:** The motor applies torque overlays to guide the steering wheel along computed trajectories, giving the driver gentle haptic cues
- **Manual Mode:** The motor acts as a force feedback device or disengages entirely, handing full control to the driver
- **Accelerator & Brake:** A potentiometer-based velocity input system was implemented to replicate the full driving interface in a compact test rig

The system was designed to smoothly transition between these modes without jarring changes in the feel of the wheel.

---

### User Study

15 participants completed a structured study evaluating:

- **Takeover time:** How quickly drivers reclaimed full control from autonomous mode
- **Steering interaction quality:** Naturalness and comfort of the haptic interface during transition
- **Effectiveness:** Trajectory deviation after handover and subjective driver confidence

The results informed our model of human-robot interaction during AV control transitions and are being published.

---

### Publication

> **A R Gurumoorthi**, V Bagaria, B Sebastian. *"Interactive steering for seamless transition during control handover in autonomous driving."* — Accepted for publication.

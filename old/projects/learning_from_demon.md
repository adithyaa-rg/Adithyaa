---
title: "Learning from Observations"
layout: default
---

## Learning from Demonstration for Agents with Mismatched Dynamics

**Advisors:** [Prof. B Ravindran](https://wsai.iitm.ac.in/~ravi/), Center for Responsible AI (CeRAI), IIT Madras  
**Mentor:** [Returaj Burnwal](https://returaj.github.io/), IIT Madras  
**Status:** Ongoing (Aug 2025 – Present)

---

### Motivation

Classical algorithmic approaches struggle with the complexity of real-world robot tasks. Even sample-efficient methods like Reinforcement Learning are prohibitively expensive when exploration happens in the real world. Imitation Learning addresses this by learning from demonstration data — but most methods require *action* information, which is often unavailable in practice.

**Learning from Observations (LfO)** is a subfield of Imitation Learning that learns purely from state sequences, without access to the demonstrator's actions or knowledge of the environment dynamics. This is more realistic: a robot watching a human perform a task cannot directly observe neural commands or joint torques.

---

### Problem Setup

I focus on the case where the imitator and demonstrator have **parametrically different dynamics** — for example, different mass, joint stiffness, or actuation profiles. This is the first step towards transfer learning in robotics, where knowledge must flow across structurally distinct agents such as quadrupeds, humanoids, or manipulators of different builds.

**Given:**
- State-only trajectory demonstrations from an expert (egocentric state sequences)
- Mixed distribution of state-action pairs from the imitator agent

**Goal:** Learn a policy for the imitator that reproduces expert behaviour, despite dynamic mismatch.

---

### Approach

<div style="display: flex; justify-content: center; gap: 5px; margin: 1.5rem 0;">
  <img src="images/learning_from_demo/step1.png" alt="Step 1: State Occupancy Matching" width="48%">
  <img src="images/learning_from_demo/step2.png" alt="Step 2: Density-based Weighting" width="48%">
</div>
<div style="display: flex; justify-content: center; margin-bottom: 1.5rem;">
  <img src="images/learning_from_demo/step3.png" alt="Step 3: Sub-trajectory Sampling and Weighted Learning" width="50%">
</div>

**Step 1 — State Occupancy Matching:** Use density estimation methods to model the expert's state distribution and compare it with the imitator's offline dataset.

**Step 2 — Density-Based Reward Assignment:** Score transitions in the imitator dataset by their likelihood under the expert distribution, and assign rewards accordingly.

**Step 3 — Sub-trajectory Sampling:** Use state sequence information (rather than individual transitions) to identify important sub-trajectories. Implement Weighted Behaviour Cloning using these scores to train the imitator policy.

---

### Why This Matters

This approach is a building block for cross-morphology robot learning: teaching a new robot not by re-collecting expert data, but by re-using state observations of a different agent. It has direct implications for humanoid and quadruped skill transfer.

---
title: "Multi-Agent RL — Battlesnakes"
layout: default
---

## Reinforcement Learning for Battlesnakes

**Course:** Multi-Agent Systems & AI (DD2438) — KTH Royal Institute of Technology  
**Advisor:** Prof. Petter Ögren  
**Duration:** April – May 2025 · Stockholm, Sweden

---

### The Problem

[Battlesnake](https://play.battlesnake.com/) is a competitive multi-agent game where snakes compete to survive and grow. The challenge involved a **two-agent cooperative team** competing against other teams — requiring agents to coordinate, avoid each other, and outwit opponents simultaneously.

This is harder than standard single-agent RL: each agent must reason about its teammate as well as multiple adversaries, all in a partially observable grid world.

---

### Approach

**Reward Design**  
Standard survival reward signals are sparse and slow to learn from. We designed dense custom reward functions that penalise proximity to walls and other snakes, incentivise food collection in early game, and reward strategic head positioning in late game.

**PPO and DQN Baselines**  
We trained two policy architectures — Proximal Policy Optimisation (PPO) and Deep Q-Networks (DQN) — and compared their convergence and final performance.

**Curriculum Learning**  
Rather than training against strong opponents from the start, we designed a staged curriculum:
- Stage 1: Rule-based opponent (easy)
- Stage 2: Trained PPO agent (medium)
- Stage 3: Competition-level opponents (hard)

This significantly improved sample efficiency and policy quality.

**Team Coordination**  
Each agent had its own policy, but we added a **policy divergence constraint** within the team to prevent the two agents from specialising too far apart — ensuring they remained capable of covering for each other.

---

### Findings

Failure analysis revealed two key issues:
- **Replay buffer sampling:** Uniform replay overweighted common low-risk states, causing agents to be poorly calibrated in high-stakes endgame scenarios
- **Model complexity:** Larger networks for DQN led to unstable Q-value estimates and reduced performance relative to the smaller PPO network

These insights suggest that prioritised experience replay and careful architecture search are critical for multi-agent competitive RL.

---
title: Learning from Demonstration for Agents with Mismatched Dynamics
layout: default
---
## Learning from Demonstration for Agents with Mismatched Dynamics

Advisor: [B Ravindran](https://wsai.iitm.ac.in/~ravi/), [Center for Responsible AI](https://cerai.iitm.ac.in/), IIT Madras

### Problem Statement
Develop a model based approach to tackle the problem of Learning from Observations. Given the trajectories of expert demonstrators traversing a given environment, we aim to learn the policy for an imitator agent, with possibly different dynamics to act in that environment.

We are given trajectories of demonstrator experts and we are given mixed distribution trajectories of state-action pairs for the imitator agent.

![Reference: SMODICE: Versatile Offline Imitation Learning via State Occupancy Matching](https://lh3.googleusercontent.com/sitesv/AICyYdZ6lSPcst8pBQhDq2rz3XZQ5f82WG-c_W7JKtPKqLtbsRaasCJ4t4xdlY0P5KvcasePiDH8SCMFhre69Kxvl_6t2IEC8ovkeh4oUs0JZtjj2Et0aweuLSvCClXId5VIfpq0NYQkWPHk8rI7mxSmKCuy8Qk_7e1wNzMTYp4rLWzL2y-8c0gyLqeRWnUsOmdDf2H8tooYSIGxXvUNfVj_s3XCvjRaLeukrmOSJA4=w1280)
**Reference**: SMODICE: Versatile Offline Imitation Learning via State Occupancy Matching

### Current Progress
I am currently working on literature review to formulate the methodology and starting to implementation currently. I am working to integrate a model to enhance the learning and use state occupancy matching to learn the important states from the expert demonstrations.
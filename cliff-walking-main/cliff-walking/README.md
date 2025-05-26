# Cliff Walking – Reinforcement Learning

This project offers a Python implementation of the classic **Cliff Walking** problem, as presented in Example 6.6 of *Reinforcement Learning: An Introduction* by Sutton & Barto. It demonstrates various reinforcement learning algorithms including:

- **Temporal Difference (TD(0))**
- **Q-Learning**
- **Expected SARSA**

---

## Overview

The Cliff Walking problem is a gridworld scenario where an agent must navigate from a start point to a goal, avoiding the cliff region that yields a significant negative reward. It is a standard testbed for evaluating reinforcement learning algorithms.

---

## Implemented Algorithms

- **TD(0) Policy Evaluation**  
  Estimates the value function for a given policy using temporal difference learning.

- **Q-Learning**  
  An off-policy algorithm that learns the optimal action-value function.

- **Expected SARSA**  
  An on-policy algorithm that updates the action-value function based on the expected value over all possible actions.

---

## Environment Details

- **Grid Size**: 4x12 grid
- **Start State**: Bottom-left corner
- **Goal State**: Bottom-right corner
- **Cliff Region**: Bottom row between start and goal
- **Actions**: Up, Down, Left, Right
- **Rewards**:
  - Step: -1
  - Falling off cliff: -100 (resets to start state)

---

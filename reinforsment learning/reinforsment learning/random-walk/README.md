# 🚶‍♂️ Random Walk – Reinforcement Learning Experiments

This project implements and compares classic reinforcement learning algorithms on the **Random Walk** problem, as introduced in Sutton & Barto’s *Reinforcement Learning: An Introduction*.

---

## 📌 Problem Overview

The **Random Walk** environment is a linear chain of states with terminal states at both ends.  
An agent starts in the center and moves left or right with equal probability until it reaches a terminal state.

**Objective:** Learn the value of each non-terminal state — the expected return starting from that state under the random policy.

---

## 🧠 Implemented Algorithms

- **Monte Carlo (MC) Prediction** 🎲  
  Estimates value functions by averaging returns after each visit to a state.

- **Temporal Difference (TD(0))** ⏱️  
  Bootstraps value estimates using the difference between successive predictions.

- **n-step TD** ➡️➡️  
  Extends TD(0) to use updates over multiple steps for a balance between MC and TD.

- **TD(λ)** 🧮  
  Combines MC and TD using eligibility traces and a decay parameter λ.

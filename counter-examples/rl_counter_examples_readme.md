# Counter-Examples

This directory contains materials that expose weaknesses, edge cases, and failure modes in reinforcement learning algorithms. The goal is to provide clear, reproducible examples that help identify where standard methods break down and why.

## Directory Structure

### 📁 `/src`
Implementations of counter-example environments, algorithm variants, and supporting utilities.

### 📁 `/notebooks`
Interactive notebooks showcasing experiments, reproducing counter-examples, and providing step-by-step analysis.

### 📁 `/book_images`
Reference figures and diagrams collected from academic papers and textbooks.

### 📁 `/generated_images`
Plots, visualizations, and illustrations produced during experiments.

## Overview
This project investigates well-known failure modes in value-based reinforcement learning, with a focus on Baird's counterexample and modern solutions that address divergence. It is designed so the reader can immediately understand **what breaks, why it breaks, and how newer algorithms fix it**.
Reinforcement learning methods often show strong empirical results, yet they can fail unexpectedly under specific conditions. This collection focuses on:

- **Concrete counter-examples** where well-known algorithms behave suboptimally
- **Code and environments** enabling full reproduction of results
- **Comparisons** between theoretical expectations and observed behavior
- **Explanations** detailing why each failure occurs and what it teaches

These materials highlight limitations in exploration, convergence, function approximation, and stability.

## Included Counter-Examples and Notebooks

### **1. Baird's Counterexample (bairds_counterexample.ipynb)**
A classic example demonstrating that standard **TD(0)** with linear function approximation can diverge even in a simple, deterministic Markov process. The notebook:
- Builds Baird’s “star” MDP
- Shows how TD updates push weights away from the correct solution
- Visualizes parameter divergence step-by-step
- Highlights why off-policy bootstrapping is unstable

### **2. Emphatic TD (emphatic_baird.ipynb)**
This notebook demonstrates how **Emphatic TD (ETD)** stabilizes learning using emphasis weights. It:
- Implements the ETD update rule
- Shows that weights converge even in Baird’s environment
- Provides visual comparison against divergent TD results
- Explains the role of importance sampling and emphasis

### **3. TDC / GTD2 (tdc_baird.ipynb)**
A demonstration of gradient-corrected temporal difference learning. This notebook:
- Implements the TDC/GTD2 algorithm
- Shows stable convergence on the same counterexample
- Demonstrates how the secondary weight vector corrects divergence
- Compares learning curves with ETD and standard TD

These three notebooks give the reader a full picture: **what breaks, how to detect it, and which algorithms solve the issue.**

## Getting Started
1. Start with the notebooks in `/notebooks` to explore each counter-example interactively.
2. Dive into the implementations under `/src` to understand how environments and agents are built.
3. Compare experimental visuals in `/generated_images` with reference figures in `/book_images`.

## Contributing
To add a new counter-example:
1. Describe the theoretical motivation and what algorithmic weakness it illustrates.
2. Add reproducible code in `/src`.
3. Create a notebook demonstrating the failure and explaining the result.
4. Include relevant plots or diagrams in `/generated_images`.

---
*Updated: 2025-11-16*


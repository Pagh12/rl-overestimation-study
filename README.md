# RL Bias Benchmark

This repository contains experiments on **overestimation bias** in deep reinforcement learning (RL) algorithms.  
The project compares several Q-learning variants across multiple environments and tracks both **cumulative returns** and **estimation bias**.

---

## Algorithms Implemented
- **DDQN** – Double Deep Q-Network  
- **DDQN_MIN** – DDQN variant with bias-reducing modification  
- **Q-Ensemble-MIN** – Ensemble-based Q-learning with conservative estimates  
- **REDQ** – Randomized Ensembled Double Q-learning  

---

## Environments
Custom lightweight environments designed for controlled experiments:
- **MountainClimb**  
- **BranchingTree**  
- **SlotMachineChain**

---

## Features
- Train and evaluate multiple RL agents on different environments.  
- Track **cumulative reward** across episodes.  
- Measure **overestimation bias** at evaluation checkpoints.  
- Support for configurable ensemble sizes (Q-Ensemble and REDQ).  
- Automatic saving of plots to `Results/` for both reward and bias.

---
## Limitations & Reflections
Based on the presented results (Figures 1–6), it is not possible to conclude that the models are appropriately implemented.  

Some models appear to increase their returns during training, while others unexpectedly decrease. The latter behavior is typically only possible if the implementation is incorrect.  

Similarly, the estimation biases reach very high values (e.g., 1200–1400 as in Figure 3), which is far beyond theoretical expectations.  

These outcomes confirm that the current implementation pipeline is **not fully sound** and should be considered a **work-in-progress** rather than a finalized benchmark.


---

## Installation
Clone the repository and install dependencies:

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
pip install -r requirements.txt


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

## Installation
Clone the repository and install dependencies:

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
pip install -r requirements.txt

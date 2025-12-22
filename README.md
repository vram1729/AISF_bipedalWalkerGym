# BipedalWalker-v3 Optimized Soft Actor-Critic (SAC) Agent

This repository contains a high-performance Reinforcement Learning (RL) agent capable of solving the **BipedalWalker-v3** environment with a consistent score of **300+**. 

The project focuses on using the **Soft Actor-Critic (SAC)** algorithm with automatic entropy tuning and observation normalization to achieve a smooth, energy-efficient walking gait.

## 📊 Performance Results
- **Peak Reward:** 303.42
- **Average Reward (Solved):** ~295.0
- **Status:** Environment Solved (Threshold > 300)

![Training Progress](./results/sac_performance_graph.png)

## 🛠 Technical Specifications & Hyperparameters
The agent utilizes a twin-critic approach with an entropy-based exploration strategy. This ensures the walker does not converge on a "safe" but inefficient gait too early.

| Hyperparameter | Value | Description |
| :--- | :--- | :--- |
| **Algorithm** | SAC | Off-policy Actor-Critic |
| **Network Arch** | [400, 300] | MLP with ReLU activations |
| **Learning Rate** | 3e-4 | Adam Optimizer |
| **Batch Size** | 256 | Samples per update |
| **Ent. Coef ($\alpha$)** | 'auto' | Automatic Exploration Tuning |
| **Tau ($\tau$)** | 0.005 | Soft target update coefficient |
| **Buffer Size** | 500,000 | Experience Replay memory |



## 📁 Repository Structure
- `/notebooks`: Contains the Google Colab `.ipynb` used for training.
- `/models`: Contains the final model weights (`.zip`) and normalization stats (`.pkl`).
- `/results`: Training graphs, logs, and a demo video of the 303-score run.

## 🚀 How to Reproduce
To run the pre-trained agent on your local machine or in Colab:

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git](https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git)
   cd YOUR_REPO_NAME

# MCDM-DQN: Adaptive Replay Buffer Management via VIKOR

This repository contains the source code for the continuous-control (HalfCheetah-v5) experiments reported in **Section 4.9.5** of the manuscript: *"Replay Buffer Management in Deep Reinforcement Learning: A Multi-Criteria Decision-Making Approach"*.

The proposed framework, **MCDM-DQN (VIKOR)**, integrates four replay prioritization criteria (TD-error, reward magnitude, novelty, and recency) within an adaptive VIKOR-based weighting mechanism to improve learning stability and performance in Deep Reinforcement Learning.

##  Repository Contents

- `MCDM_DQN.ipynb`: The main Jupyter Notebook containing both the setup instructions (MuJoCo installation) and the full experiment code (training, evaluation, and statistical analysis).
- `README.md`: This file.

##  Requirements

The code was developed and tested with the following environment:
- **Python**: 3.10
- **PyTorch**: 2.0
- **Gymnasium**: 0.29.1 (with MuJoCo support)
- **Hardware**: Runs efficiently on CPU (Intel Core i5, 12 GB RAM) without GPU acceleration.

##  How to Run (in Google Colab)

1. Open `MCDM_DQN.ipynb` in Google Colab.
2. Run the first cell to install and configure MuJoCo and Gymnasium (if you haven't installed them yet).
3. Run the subsequent cells to train the DQN, PER, and MCDM-DQN models for 10 independent runs. The notebook will automatically generate and save the raw data (Excel files) and statistical reports, and trigger a download of the results at the end.

##  Reproducibility

To ensure full reproducibility of the results reported in Section 4.9.5:
- The random seeds are fixed (`SEED = 42`).
- All models share identical hyperparameters, network architectures, and replay buffer capacities.
- The specific configurations for the MCDM-DQN are detailed in the manuscript (Section 4.2).

## 📝 Citation

If you use this code in your research, please cite our manuscript:
*(Citation details will be added upon publication)*

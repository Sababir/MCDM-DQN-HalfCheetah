# MCDM-DQN: Adaptive Replay Buffer Management via VIKOR

This repository contains the source code for the continuous-control (HalfCheetah-v5) experiments reported in **Section 4.9.5** of the manuscript: *"Replay Buffer Management in Deep Reinforcement Learning: A Multi-Criteria Decision-Making Approach"*.

The proposed framework, **MCDM-DQN (VIKOR)**, integrates four replay prioritization criteria (TD-error, reward magnitude, novelty, and recency) within an adaptive VIKOR-based weighting mechanism to improve learning stability and performance in Deep Reinforcement Learning.

##  Repository Contents

- `setup_environment.py`: Script to install and configure MuJoCo and Gymnasium in Google Colab.
- `halfcheetah_experiment.py`: The main script to train the models and reproduce the results reported in Section 4.9.5.
- `README.md`: This file.

##  Requirements

The code was developed and tested with the following environment:
- **Python**: 3.10
- **PyTorch**: 2.0
- **Gymnasium**: 0.29.1 (with MuJoCo support)
- **Hardware**: Runs efficiently on CPU (Intel Core i5, 12 GB RAM) without GPU acceleration.

Other required libraries (such as NumPy, Pandas, SciPy, Matplotlib) are standard in Google Colab and can be installed via `pip` if running locally.

## How to Run (in Google Colab)

1. **Setup the environment**:
   Open a new notebook in Google Colab and run the commands in `setup_environment.py` to install the required system dependencies and MuJoCo.

2. **Run the experiment**:
   Copy the contents of `halfcheetah_experiment.py` into a new cell and run it. The script will train the DQN, PER, and MCDM-DQN models for 10 independent runs. It will automatically generate and save the raw data (Excel files) and statistical reports in a local directory, and trigger a download of the results at the end of the run.

##  Reproducibility

To ensure full reproducibility of the results reported in Section 4.9.5:
- The random seeds are fixed (`SEED = 42`).
- All models share identical hyperparameters, network architectures, and replay buffer capacities.
- The specific configurations for the MCDM-DQN are detailed in the manuscript (Section 4.2).

##  Citation

If you use this code in your research, please cite our manuscript:
*(Citation details will be added upon publication)*
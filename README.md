# Cliff Walking using SARSA and Q-learning

## Overview
This project implements and compares two reinforcement learning algorithms for solving the Cliff Walking environment:

- **SARSA (State-Action-Reward-State-Action)**: an on-policy method that learns from the action actually taken.
- **Q-learning**: an off-policy method that learns the optimal action-value function by using the maximum future reward.

Both algorithms are applied to the same Cliff Walking environment to observe how different learning strategies navigate the grid and avoid the cliff.

## Environment Details
The environment is based on `CliffWalking-v1` from the `gymnasium` library.

* **Grid Size:** 4 rows by 12 columns (48 total states)
* **Action Space:** 4 possible moves (Up, Down, Left, Right)
* **Reward System:**
  * **Standard Step:** -1
  * **Cliff Node:** -100
  * **Goal Node:** 0

## Hyperparameters
Based on the implementation, the following parameters are used to train the agents:

* **Episodes:** 500
* **Learning Rate (Alpha):** 0.5
* **Discount Factor (Gamma):** 0.99
* **Exploration Rate (Epsilon):** 0.1

## Results
The agents successfully learn to navigate the grid while avoiding the cliff. SARSA tends to learn a more conservative policy because it updates based on the actual next action taken, while Q-learning often learns a more aggressive path toward the goal.

* **SARSA Final Converged Reward:** -17
* **Q-learning Final Converged Reward:** Typically competitive and may vary depending on the training setup and random seed

## Dependencies
* `gymnasium`
* `numpy`

## Algorithms Included
This repository includes implementations for:

* **SARSA**
* **Q-learning**

These notebooks/implementations can be used to compare the behavior, convergence, and path selection of both algorithms in the same environment.

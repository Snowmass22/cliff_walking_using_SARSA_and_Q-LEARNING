# Cliff Walking using SARSA

## Overview
This project implements the **SARSA (State-Action-Reward-State-Action)** reinforcement learning algorithm to solve the Cliff Walking environment. SARSA is an on-policy algorithm that focuses on reward maximization while learning safer trajectories. This implementation utilizes an **epsilon-greedy policy** with a 10% exploration and 90% exploitation rate to balance discovering new paths and leveraging known safe routes.

## Environment Details
The environment is based on `CliffWalking-v1` from the `gymnasium` library.
* **Grid Size:** 4 rows by 12 columns (48 total states).
* **Action Space:** 4 possible moves (Up, Down, Left, Right).
* **Reward System:**
  * **Standard Step:** -1
  * **Cliff Node:** -100
  * **Goal Node:** 0

## Hyperparameters
Based on the implementation, the following parameters are used to train the agent:
* **Episodes:** 500
* **Learning Rate (Alpha):** 0.5
* **Discount Factor (Gamma):** 0.99
* **Exploration Rate (Epsilon):** 0.1

## Results
The agent successfully learns to navigate the grid while avoiding the cliff. By heavily penalizing the cliff nodes and updating based on the action actually taken, SARSA learns a safe, conservative path to the goal. 
* **Final Converged Reward:** -17

## Dependencies
* `gymnasium`
* `numpy`

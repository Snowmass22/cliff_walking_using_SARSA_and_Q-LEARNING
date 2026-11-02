# Cliff Walking using SARSA and Q-learning

A reinforcement learning project that solves the classic `CliffWalking-v1` environment using both SARSA and Q-learning. The repository is designed to help compare how two widely used temporal-difference algorithms learn in the same environment.

## Overview
This project demonstrates how reinforcement learning agents can navigate a grid-world environment while avoiding a dangerous cliff and reaching the goal state efficiently.

The repository includes implementations for:

- SARSA (on-policy)
- Q-learning (off-policy)

These algorithms are trained on the same environment and can be compared based on behavior, convergence, and policy quality.

## Why this project?
The Cliff Walking task is a classic reinforcement learning example that highlights:

- exploration vs exploitation
- reward shaping and penalties
- policy learning under uncertainty
- differences between on-policy and off-policy learning

## Environment
The environment is based on Gymnasium's `CliffWalking-v1`.

- Grid size: 4 x 12
- Total states: 48
- Action space: Up, Down, Left, Right
- Reward structure:
  - Standard step: -1
  - Cliff cell: -100
  - Goal cell: 0

## Algorithm Comparison

| Algorithm | Type | Key idea | Typical behavior |
| --- | --- | --- | --- |
| SARSA | On-policy | Updates using the action actually taken | More conservative and cautious |
| Q-learning | Off-policy | Updates using the best estimated future action | Often more aggressive and efficient |

## Training Setup
The project uses the following default parameter values:

- Episodes: 500
- Learning rate (alpha): 0.5
- Discount factor (gamma): 0.99
- Exploration rate (epsilon): 0.1

## Repository Structure
The project is organized around implementing and experimenting with reinforcement learning agents in the Cliff Walking environment.

## Dependencies
Install the required Python libraries:

```bash
pip install gymnasium numpy
```

## Running the Project
Clone the repository and run the notebook or script that contains the training loop for the selected algorithm.

```bash
git clone https://github.com/Snowmass22/cliff_walking_using_SARSA_algo.git
cd cliff_walking_using_SARSA_algo
```

Then run the notebook or script used for training the agent.

## Results
The agents learn to navigate the environment while avoiding the cliff. SARSA tends to produce a more cautious trajectory because it updates according to the action that was actually taken, while Q-learning often finds a more direct path toward the goal.

Example outcome:

- SARSA converged reward: approximately -17
- Q-learning performance varies depending on the training setup and random seed

## Project Goal
This repository is useful for understanding:

- how value-based RL algorithms behave in maze-like environments
- how policy updates differ between SARSA and Q-learning
- how reward penalties influence navigation behavior

## License
This project is intended for educational and experimental use in reinforcement learning.

## Contributing
Contributions, suggestions, and improvements are welcome. If you want to extend the project, consider adding:

- visualizations of training progress
- comparison plots for cumulative reward
- more environments and algorithms
- additional hyperparameter tuning experiments

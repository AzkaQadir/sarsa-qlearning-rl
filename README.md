# sarsa-qlearning-rl
Tabular reinforcement learning with SARSA and Q-learning on Gymnasium environments like MountainCar and LunarLander.

🎮 Classic Control RL Agents: LunarLander & MountainCar
This repository contains two classic reinforcement learning implementations using SARSA(0), SARSA(λ), and Q-Learning to solve:
🌙 LunarLander-v3 (Box2D environment)
🏔️ MountainCar-v0 (Classic Control environment)
All agents use tabular methods on discretized state spaces and visualize their training progress and performance using plots and rendered videos.

📁 Files:
File	Description:
LunarLander_Agent.py	RL agent for LunarLander-v3 using SARSA(0), Q-Learning, and SARSA(λ)
MountainCar_Agent.py	RL agent for MountainCar-v0 using the same three algorithms

📦 Requirements:
Install the following dependencies:
pip install gymnasium[box2d] matplotlib tqdm moviepy
✅ Ensure swig is installed for Box2D environments to run correctly.

🧠 Algorithms Implemented:
All three agents support the following temporal-difference algorithms:
SARSA(0) – On-policy learning using bootstrapped updates
Q-Learning – Off-policy method using the greedy action
SARSA(λ) – On-policy learning with eligibility traces

🔍 Shared Features:
Discretization of Continuous States: Converts high-dimensional continuous state space into discrete bins for tabular Q-learning.
Epsilon-Greedy Policy: Controls the exploration-exploitation trade-off.
Performance Tracking: Episode returns and smoothed average curves.
Video Rendering: Records trained agent episodes as MP4 videos.

🌙 LunarLander-v3 Overview:
State Space: 8 continuous variables (position, velocity, angle, leg contact)

#Action Space: 4 discrete actions:
Goal: Land the lunar module safely between flags with zero velocity
Run:  python LunarLander_Agent.py
Example Outputs
Line plots showing episode rewards and moving averages


🏔️ MountainCar-v0 Overview:
State Space: 2 continuous values (position, velocity)
Action Space: 3 actions (push left, no push, push right)
Goal: Drive the underpowered car up the hill using momentum
Run:  python MountainCar_Agent.py
Example Outputs
Reward trends showing convergence to the goal


📊 Visualization Example:
Training performance is visualized using reward trends:
Smoothed using a moving average window
Clearly compares convergence behavior of each algorithm

⚙️ Hyperparameters to Tune:
ALPHA: Learning rate
GAMMA: Discount factor
EPSILON: Exploration rate
LAMBDA: Eligibility trace decay for SARSA(λ)
Number of bins for discretization

📚 References:
Sutton & Barto, Reinforcement Learning: An Introduction
OpenAI Gymnasium Docs
Box2D LunarLander Environment

✅ Future Improvements:
Replace tabular methods with deep Q-networks (DQN)
Implement reward shaping for faster convergence
Experiment with adaptive exploration and learning rates

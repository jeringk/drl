# Introduction to Reinforcement Learning (RL)

- **Examples**  
  Applications in robotics, game playing (e.g., AlphaGo), recommendation systems, and autonomous vehicles.

## Elements of Reinforcement Learning

- **Policy**  
  The agent’s strategy for selecting actions, mapping states to actions.
- **Reward**  
  Scalar feedback signal indicating the immediate benefit of an action.
- **Value**  
  Expected long-term return from a state or state-action pair.
- **Model of the Environment**  
  The agent’s representation of how the environment behaves (transition and reward functions).

*Characteristics and examples for each element.*

---

## Multi-Armed Bandit Problem

- **Motivation and Problem Statement**  
  Choosing between multiple options (arms) with unknown rewards to maximize total reward.
- **Incremental Solution** to the stationary & non-stationary MAB problems  
  Updating value estimates incrementally as new data arrives; adapting to changing reward distributions.
- **Exploration vs. Exploitation Tradeoff**  
  Balancing trying new actions (exploration) and leveraging known rewarding actions (exploitation).
- **Bandit Gradient Algorithm** as Stochastic Gradient Ascent  
  Learning preferences for actions using gradient ascent on expected reward.
- **Associative Search**  
  Contextual bandits: selecting actions based on observed context or state.

---

## (Finite) Markov Decision Processes (MDP)

- **Modelling Agent-Environment Interaction using MDP**  
  Formalizing RL problems with states, actions, transition probabilities, and rewards.
- **Examples**  
  Gridworld, navigation tasks, inventory management.
- **Goals, Rewards & Returns**  
  Maximizing cumulative reward (return) over time.
- **Policy and Value Functions**  
  Policy: mapping from states to actions; Value functions: expected return from states or state-action pairs.
- **Bellman Equation for Value Functions**  
  Recursive relationships for value functions, foundational for many RL algorithms.
- **Optimal Policy and Optimal Value Functions**  
  Policies and value functions that maximize expected return.

---

## Dynamic Programming

- **Introduction**  
  Solving MDPs with known models using recursive computation.
- **Policy Iteration**  
  Alternating policy evaluation and improvement to find optimal policies.
- **Value Iteration**  
  Iteratively updating value functions to converge to optimal values.
- **Generalised Policy Iteration**  
  Framework combining policy evaluation and improvement in various ways.
- **Efficiency of Dynamic Programming**  
  Computational considerations and limitations (e.g., curse of dimensionality).

---

## Monte Carlo Methods

- **Prediction**  
  Estimating value functions from sample episodes.
- **Estimation of Action Values**  
  Learning action-value functions directly from experience.
- **Monte Carlo Control**  
  Improving policies using Monte Carlo estimates.
- **Off-policy Prediction via Importance Sampling**  
  Learning about one policy while following another using weighted samples.
- **Off-policy Monte Carlo Control**  
  Combining off-policy learning with control.

---

## Temporal Difference (TD) Learning

- **TD Prediction**  
  Learning value functions by bootstrapping from current estimates.
- **On-policy TD Model-Free (SARSA)**  
  Learning action values while following the current policy.
- **Off-policy TD Model-Free (Q-Learning)**  
  Learning optimal action values independent of the policy being followed.
- **Expected SARSA**  
  Using expected value over all possible actions for updates.
- **N-step TD Policy Evaluation**  
  Using returns over multiple steps to update value estimates.
- **N-step SARSA**  
  Extending SARSA to use multi-step returns.
- **Off-policy N-step SARSA**  
  Combining multi-step returns with off-policy learning.

---

## Function Approximation

- **Feature Construction for Linear Methods**  
  Creating features to represent states or state-action pairs.
  - Tile Coding: Partitioning state space into overlapping regions.
  - Asymmetric Tile Coding: Using non-uniform tiles for better representation.
- **Linear Function Approximation**  
  Approximating value functions as linear combinations of features.
- **Semi-Gradient TD Methods**  
  Using gradients for updates when function approximation is used.
- **Off-policy Function Approximation**  
  Challenges and solutions for combining off-policy learning with function approximation.

---

## Deep Reinforcement Learning

- **Deep Q Network (DQN)**  
  Using deep neural networks to approximate Q-values.
- **Double DQN**  
  Reducing overestimation bias in DQN.
- **Rainbow**  
  Combining multiple DQN improvements (e.g., prioritized replay, dueling networks).

---

## Policy Gradient Methods

- **Policy Gradient Theorem**  
  Theoretical foundation for directly optimizing policies.
- **REINFORCE Algorithm**  
  Monte Carlo policy gradient method.
- **REINFORCE with Baseline Algorithm**  
  Reducing variance in policy gradient estimates using a baseline.
- **Actor-Critic Methods**  
  Combining value function (critic) and policy (actor) learning.
- **REINFORCE for Continuing Problems (No Episode Boundaries)**  
  Adapting policy gradients for ongoing tasks.

---

## Other Topics

- **Monte-Carlo Tree Search**  
  Planning algorithm using random sampling of future actions.
- **AlphaGo, AlphaGo Zero, MuZero**  
  Landmark RL systems for board games and planning without explicit models.
- **Imitation Learning**  
  Learning policies from demonstrations.

---

## Special Sessions

- **Multi-Agent RL**  
  Learning in environments with multiple interacting agents.
- **Human-in-the-Loop (HITL) Learning**  
  Incorporating human feedback into RL.
- **Safety in RL**  
  Ensuring safe exploration and deployment of RL agents.
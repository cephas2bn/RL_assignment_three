# Reinforcement Learning in Gridworld: SARSA, Q-learning, and Value Function Approximation

## Project Overview
This project explores and compares various reinforcement learning algorithms within a gridworld environment, focusing on two main parts:
1. **Policy Learning with SARSA and Q-learning**: Implementation and comparison of the SARSA and Q-learning algorithms to learn optimal policies in a gridworld environment.
2. **Value Function Approximation**: Estimation and comparison of value functions using the Gradient Monte Carlo method, Semi-Gradient TD(0) method, and Exact Value Function.

## Part 1: Policy Learning with SARSA and Q-learning
### SARSA
This on-policy algorithm updates the Q-values based on the action actually taken by the policy. It learns the value function while following the current policy, incorporating the agent's exploration strategy into the learning process.

### Q-learning
This off-policy algorithm updates the Q-values assuming that the agent will follow the optimal policy in the future, regardless of the current policy. It learns the optimal value function by assuming the best possible action will be taken at each step.

### Implementation
Both SARSA and Q-learning were implemented and used to learn optimal policies in a 5x5 gridworld environment. The learned policies were then analyzed and compared.

## Part 2: Value Function Approximation
### Exact Value Function
The Exact Value Function was computed using Bellman equations, serving as a benchmark for evaluating the accuracy of the approximate methods.

### Gradient Monte Carlo Method
This a Model-free, Monte Carlo-based method that estimates the value function based on the average return observed over complete episodes. It is unbiased but can exhibit high variance in its estimates.

### Semi-Gradient TD(0) Method with Affine Function Approximation
This is also a Model-free, Temporal Difference-based method that approximates the value function using an affine function and updates the weights incrementally based on the temporal difference error. It is more stable and converges faster than the Monte Carlo method, though it may have a slight bias.

### Results
The Semi-Gradient TD(0) method provided a more stable and accurate approximation of the value function compared to the Gradient Monte Carlo method, which showed higher variance and less consistent estimates.

## Conclusion
This project demonstrated the effectiveness of SARSA and Q-learning in learning policies within a gridworld environment, with each method showing its strengths depending on the learning scenario. In terms of value function approximation, the Semi-Gradient TD(0) method was more reliable and closely aligned with the Exact Value Function compared to the Gradient Monte Carlo method.

## References
1. **Sutton, R. S., & Barto, A. G. (2018).** *Reinforcement Learning: An Introduction* (2nd ed.). MIT Press.
2. **Szepesvári, C. (2010).** *Algorithms for Reinforcement Learning*. Morgan & Claypool Publishers.

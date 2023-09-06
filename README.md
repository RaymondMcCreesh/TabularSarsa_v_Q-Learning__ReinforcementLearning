
## Cliff Walking Grid World README

---

### Overview

In this personal project, I delve into the world of reinforcement learning, specifically comparing two popular algorithms - **Sarsa** and **Q-learning**. The problem in focus is the classic **Cliff Walking Grid World**. This problem provides a structured environment where the impact of exploration versus exploitation trade-offs can be clearly observed.

---

### Environment Description

The Cliff Walking Grid World is a 4x12 grid. An agent starts from the bottom left and has to reach the bottom right. The catch is that the bottom row (except the starting and ending positions) represents a cliff. Walking into any of these cells incurs a substantial negative reward, effectively simulating a fall off the cliff. The agent has four potential actions at each cell: move up, down, left, or right. The task is to find a policy that allows the agent to reach the goal with the maximum cumulative reward, ideally avoiding the cliff.

---

### Algorithms

1. **Sarsa (State-Action-Reward-State-Action):** 
    - This is an on-policy temporal difference learning algorithm.
    - The agent learns by updating its Q-values using the current state, action taken, reward received, and the next state-action pair.
    - Sarsa tends to be more conservative in exploration, especially in environments with penalties or dangers like the cliff. This is because it takes into account the action that will be taken next (which is based on the current policy) when updating its Q-values.

2. **Q-learning:**
    - This is an off-policy temporal difference learning algorithm.
    - The agent learns by updating its Q-values using the current state, action taken, reward received, and the maximum Q-value of the next state (across all actions).
    - Q-learning aims to find the optimal policy that achieves the maximum cumulative reward. It's more explorative and can sometimes take risky paths if it deems the potential reward is worth it.

---

### Observations and Results

Upon running the algorithms multiple times, it was observed that:
- The agent using Sarsa often took a safer path, avoiding the cliff's edge.
- The agent using Q-learning sometimes took paths closer to the cliff, exploring if there's a quicker route to the goal even if it's riskier.

---

### Benefits of Deep Learning Methods Employed

- **Adaptability**: Both Sarsa and Q-learning adjust and learn optimal policies based on the rewards received. This makes them adaptable to different environments.
  
- **Trade-offs between Exploration and Exploitation**: These algorithms inherently manage the trade-off between exploring new paths and exploiting known paths to achieve the highest cumulative reward.
  
- **Efficiency**: Over multiple episodes, the agent refines its policy, often finding more efficient paths to the goal.

---

This project was a deep dive into understanding the nuances of reinforcement learning and how different algorithms approach the problem of learning an optimal policy in an environment with clear and immediate penalties. By comparing Sarsa and Q-learning, I gained insights into how each algorithm's approach impacts the paths chosen by the agent.

---

**Note**: The visualizations and code snippets in the notebook provide a clearer understanding of the environment setup and the results of each algorithm.

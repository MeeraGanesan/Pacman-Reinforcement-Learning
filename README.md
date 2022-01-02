# Pacman-Reinforcement-Learning

Note: Code is kept private, can show on a need-to-know basis. Attributed to UC Berkeley (http://ai.berkeley.edu)

This project implements value iteration and Q-learning to help Pacman reach the goal state.
1. Value Iteration:
- Asynchronous value iteration: The value iteration agent is an offline planner. It takes an MDP on construction and runs value iteration for the specified number of iterations. So, when a state’s value is updated in iteration k based on the values of its successor states, the successor state values used in the value update computation are those from iteration k-1. A synthesized policy is then returned from the values computed in the last iteration.
- Prioritized sweeping value iteration: This algorithm attempts to focus on updates of state values in ways that are likely to change the policy. It takes a error tolerance as input to decide whether or not to update a value. The algorithm maintains a priority queue to keep track of states that need to be updated. Values with a greater difference between 2 iterations are prioritized.

2. Q-Learning:

- The agent learns from trial-and-error by interacting with the environment. It uses epsilon-greedy action selection, where the agent chooses a random action epsilon fraction of the time and follows its current best Q-values otherwise. The final Q-values are used to determine the action Pacman would take to reach the goal state.



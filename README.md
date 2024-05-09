# SARSA Learning Algorithm


## AIM
To develop a Python program to find the optimal policy for the given RL environment using SARSA-Learning and compare the state values with the Monte Carlo method.

## PROBLEM STATEMENT
The bandit slippery walk problem is a reinforcement learning problem in which an agent must learn to navigate a 7-state environment in order to reach a goal state. The environment is slippery, so the agent has a chance of moving in the opposite direction of the action it takes.

## SARSA LEARNING ALGORITHM

States
The environment has 7 states:

Two Terminal States:
G: The goal state
H: A hole state.
Five Transition states / Non-terminal States including S: The starting state.
Actions
The agent can take two actions:

R: Move right.
L: Move left.
Transition Probabilities
The transition probabilities for each action are as follows:

50% chance that the agent moves in the intended direction.
33.33% chance that the agent stays in its current state.
16.66% chance that the agent moves in the opposite direction.
For example, if the agent is in state S and takes the "R" action, then there is a 50% chance that it will move to state 4, a 33.33% chance that it will stay in state S, and a 16.66% chance that it will move to state 2.

Rewards
The agent receives a reward of +1 for reaching the goal state (G). The agent receives a reward of 0 for all other states.

Graphical Representaion

![image](https://github.com/NivethaKumar30/sarsa-learning/assets/119559844/0d9fa57a-c368-49a7-be24-994a591b1027)


## SARSA LEARNING FUNCTION

1.Initialize the Q-values arbitrarily for all state-action pairs.
2.Repeat for each episode:
->Initialize the starting state.
->Repeat for each step of episode:
   ->Choose action from state using policy derived from Q (e.g., epsilon-greedy).
   ->Take action, observe reward and next state.
   ->Choose action from next state using policy derived from Q (e.g., epsilon-greedy).
   ->Update Q(s, a) := Q(s, a) + alpha * [R + gamma * Q(s', a') - Q(s, a)]
   ->Update the state and action.
   ->Until state is terminal.
3.Until performance converges.

## OUTPUT:
Mention the optimal policy, optimal value function , success rate for the optimal policy.

Include plot comparing the state value functions of Monte Carlo method and SARSA learning.

## RESULT:

Thus the optimal policy for the given RL environment is found using SARSA-Learning and the state values are compared with the Monte Carlo method.

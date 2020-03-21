## Navigation Project

#### Introduction

This project uses Deep Reinforcement Learning to train an AI agent to navigate the virtual environment shown below and collect yellow bananas, while avoiding the blue bananas.

![Virtual Environment](https://github.com/christos-pan/deep-reinforcement-learning/blob/master/Navigation/navigation-virtual-world.gif)

#### Environment

The environment is based on the Unity ML-Agents toolkit.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. Four discrete actions are available, corresponding to:
* 0 - move forward.
* 1 - move backward.
* 2 - turn left.
* 3 - turn right.

#### Training goal

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of the agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The task is episodic, and in order to solve the environment, the agent must get an average score of +13 over 100 consecutive episodes.


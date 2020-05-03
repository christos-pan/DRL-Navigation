## Collaboration and Competition project

#### Introduction

This project uses Deep Reinforcement Learning to train a pair of agents to control 2 tennis rackets in the environment shown below.
The goal is to pass the ball over the net back and forth, without letting it drop to the ground or go out of bounds.

![Virtual Environment](https://github.com/christos-pan/deep-reinforcement-learning/blob/master/Collaboration-And-Competition/tennis.png)

#### Environment

The environment is based on the Unity ML-Agents toolkit.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

#### Training goal

If an agent hits the ball over the net, it receives a reward of +0.1. 
If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01.

The task is episodic, and in order to solve the environment, the agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents in each episode).

#### Dependencies

The solution has the following dependencies:
1. **IPython**. The code is provided as a IPython notebook (Python 3). Please follow [these instructions](https://ipython.org/install.html) to install it. 
2. **Project dependencies**. Please follow the [instructions in the DRLND GitHub repository](https://github.com/udacity/deep-reinforcement-learning#dependencies) to install Python dependencies specific to the project.
3. **Unity Environment**. Follow the link below that corresponds to your operating system to download the Unity environment. Place the file in any local folder and unzip it.
    * Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip) 
    * Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip) 
    * Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip) 
    * Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)

#### Instructions

In order to run the solution:
* Clone or download the repository
* Open "Tennis.ipynb" notebook
* **Before running the code**, change the *file_name* parameter to match the location of the Unity environment that you downloaded
* Run the code cells. When the environment is solved, you will see a plot with the scores that the agent received in each training episode 

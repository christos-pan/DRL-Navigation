## Continuous Control project

#### Introduction

This project uses Deep Reinforcement Learning to train a double-jointed arm to reach a moving target and then follow the target's location, in the virtual environment shown below.

![Virtual Environment](https://github.com/christos-pan/deep-reinforcement-learning/blob/master/Continuous-Control/reacher.gif)

#### Environment

The environment is based on the Unity ML-Agents toolkit.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

#### Training goal

A reward of +0.1 is provided for each step that the agent's hand is in the goal location.

The training simulation contains 20 identical copies of the environment that run in parallel. The task is episodic, and in order to solve the environment, the agents must get an average score of +30 over 100 consecutive episodes, and over the 20 environments.

#### Dependencies

The solution has the following dependencies:
1. **IPython**. The code is provided as a IPython notebook (Python 3). Please follow [these instructions](https://ipython.org/install.html) to install it. 
2. **Project dependencies**. Please follow the [instructions in the DRLND GitHub repository](https://github.com/udacity/deep-reinforcement-learning#dependencies) to install Python dependencies specific to the project.
3. **Unity Environment**. Follow the link below that corresponds to your operating system to download the Unity environment. Place the file in any local folder and unzip it.
    * Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip) 
    * Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip) 
    * Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip) 
    * Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

#### Instructions

In order to run the solution:
* Clone or download the repository
* Open "Continuous_Control.ipynb" notebook
* **Before running the code**, change the *file_name* parameter to match the location of the Unity environment that you downloaded
* Run the code cells. When the environment is solved, you will see a plot with the scores that the agent received in each training episode 

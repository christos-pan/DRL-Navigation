## Navigation project

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

#### Dependencies

The solution has the following dependencies:
1. **IPython**. The code is provided as a IPython notebook (Python 3). Please follow [these instructions](https://ipython.org/install.html) to install it. 
2. **Project dependencies**. Please follow the [instructions in the DRLND GitHub repository](https://github.com/udacity/deep-reinforcement-learning#dependencies) to install Python dependencies specific to the project.
3. **Unity Environment**. Follow the link below that corresponds to your operating system to download the Unity environment. Place the file in any local folder and unzip it.
    * Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip) 
    * Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip) 
    * Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip) 
    * Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

#### Instructions

In order to run the solution:
* Clone or download the repository.
* Open "Navigation.ipynb" notebook
* **Before running the code**, change the *file_name* parameter to match the location of the Unity environment that you downloaded
* Run the code cells. When the environment is solved, you will see a plot with the scores that the agent received in each training episode 

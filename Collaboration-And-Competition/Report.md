## Implementation details

#### Algorithm

The training algorithm is DDPG. 

The environment observation space consists of 3x8 variables for each agent, including the current and past 2 states.
The DDPG agent observes all 48 variables in each training step (2 agents x 3 states x 8 state variables).
The DDPG agent returns 4 action variables, 2 for each agent.

Agent weights are updated every 4 environment steps.

A simple but effective approach for prioritized experience replay is implemented.
* When the agent successfully hits the ball over the net, this experience is recorded multiple times in the buffer.
* Experiences after the 1st hit are recorded twice in the buffer, to shift focus more on the main gameplay during the early stages of training.

The following hyperparameters are chosen:

* BUFFER_SIZE = 3e4  
* BATCH_SIZE = 512        
* GAMMA = 0.99            
* TAU = 1e-2              
* LR_ACTOR = 1e-3         
* LR_CRITIC = 3e-3      
* UPDATE_EVERY = 4            (Update weights after this amount of steps)
* SUCCESS_REPLAY_FACTOR = 4   (Add successful actions to buffer multiple times)
* MAIN_GAME_REPLAY_FACTOR = 2 (Add experiences after 1st hit multiple times to buffer)

#### Neural network architecture (Actor)

The actor's neural networks (local and target) have the following layers:

* Fully connected layer (In 48, Out 200)
* ReLU activation layer
* Fully connected layer (In 200, Out 4)
* Tanh activation layer

#### Neural network architecture (Critic)

The critic's neural networks (local and target) have the following layers:

* Fully connected layer (In 48, Out 80)
* Leaky ReLU activation layer
* Fully connected layer (In 84, Out 80) (**Note**: The selected action is introduced at this layer)
* Leaky ReLU activation layer
* Fully connected layer (In 80, Out 40)
* Leaky ReLU activation layer
* Fully connected layer (In 40, Out 1)

#### Training results

The environment was solved in 2605 episodes.
The total rewards per episode (maximum of the 2 agents) are plotted below.

![Scores per episode](https://github.com/christos-pan/deep-reinforcement-learning/blob/master/Collaboration-And-Competition/scores_per_episode_plot.png)

#### Future work

The following ideas can be explored in the future, in order to make the training process faster:

* Further experimentation with algorithm hyperparameters
* Further experimentation with different neural network architectures
* Introduction of noise, either directly in the selected actions, or integrated into the neural network parameters
* Formal implementation of prioritized experience replay
* Training separate neural networks for the 2 environment agents

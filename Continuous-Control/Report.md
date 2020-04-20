## Implementation details

#### Algorithm

The training algorithm is DDPG, with the following hyperparameters:

* BUFFER_SIZE = 1e6  
* BATCH_SIZE = 512        
* GAMMA = 0.99            
* TAU = 1e-2              
* LR_ACTOR = 1e-3         
* LR_CRITIC = 3e-3        

#### Neural network architecture (Actor)

The actor's neural networks (local and target) have the following layers:

* Fully connected layer (In 33, Out 120)
* ReLU activation layer
* Fully connected layer (In 120, Out 4)
* Tanh activation layer

#### Neural network architecture (Critic)

The critic's neural networks (local and target) have the following layers:

* Fully connected layer (In 33, Out 50)
* Leaky ReLU activation layer
* Fully connected layer (In 54, Out 50) (**Note**: The selected action is introduced at this layer)
* Leaky ReLU activation layer
* Fully connected layer (In 50, Out 20)
* Leaky ReLU activation layer
* Fully connected layer (In 20, Out 1)

#### Training results

The environment was solved in 457 episodes, with a maximum of 400 steps per episode.
The total rewards per episode (averaged over the 20 environments) are plotted below.

![Scores per episode](https://github.com/christos-pan/deep-reinforcement-learning/blob/master/Continuous-Control/scores_per_episode_plot.png)

#### Future work

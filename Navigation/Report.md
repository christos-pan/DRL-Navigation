## Implementation details

#### Algorithm

The training algorithm is Double DQN, with the following hyperparameters:

* BUFFER_SIZE = int(1e5)
* BATCH_SIZE = 64
* GAMMA = 0.99
* TAU = 1e-3
* LR = 5e-4
* UPDATE_EVERY = 4
* eps_start = 1.0
* eps_end = 0.01
* eps_decay = 0.995

#### Neural network architecture

The solution's neural networks (local and target) have the following layers:

* Fully connected layer (In 37, Out 100)
* ReLU activation layer
* Dropout layer (rate = 0.2)
* Fully connected layer (In 100, Out 50)
* ReLU activation layer
* Dropout layer (rate = 0.2)
* Fully connected layer (In 50, Out 4)

#### Training results

The environment was solved in 457 episodes, with a maximum of 400 steps per episode.
The total rewards per episode are plotted below.

![Scores per episode](https://github.com/christos-pan/deep-reinforcement-learning/blob/master/Navigation/scores-per-episode-plot.png)

#### Future work

The following ideas can be explored in the future, in order to make the training process faster:

* Further experimentation with algorithm hyperparameters
* Further experimentation with different neural network architectures
* Implementation of more advanced improvements of the DQN algorithm, e.g. dueling DQN, prioritized experience replay or a combination of them (and possibly others), e.g. rainbow algorithm

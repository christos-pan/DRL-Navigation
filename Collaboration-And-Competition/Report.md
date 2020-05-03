## Implementation details

#### Algorithm

The training algorithm is DDPG. 
Agent weights are updated every 4 steps.

The environment observation space consists of 3x8 variables for each agent, including the current and past 2 states.
The DDPG agent observes all 48 variables in each training step (2 agents x 3 steps x 8 state variables).
The DDPG agent returns 4 action variables, 2 for each agent.

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


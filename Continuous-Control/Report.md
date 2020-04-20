## Implementation details

#### Algorithm

The training algorithm is DDPG, with the following hyperparameters:

* BUFFER_SIZE = int(1e6)  
* BATCH_SIZE = 512        
* GAMMA = 0.99            
* TAU = 1e-2              
* LR_ACTOR = 1e-3         
* LR_CRITIC = 3e-3        


## Implementation details

The training algorithm is Double DQN, with the following hyper-parameters:

* BUFFER_SIZE = int(1e5)
* BATCH_SIZE = 64
* GAMMA = 0.99
* TAU = 1e-3
* LR = 5e-4
* UPDATE_EVERY = 4
* eps_start = 1.0
* eps_end = 0.01
* eps_decay = 0.995


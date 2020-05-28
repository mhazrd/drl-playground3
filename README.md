[//]: # (Image References)

[image1]: https://video.udacity-data.com/topher/2018/May/5af7955a_tennis/tennis.png "Trained Agent"

# Deep RL Project: Collaboration and Competition (Tennis)

## Introduction

The project's objective is to train an agent to move each player (racket) to hit a ball properly so that the ball is kept in the air and within the tennis court. The sample image of the Unity **Tennis** environment is shown below.

![Trained Agent][image1]

Each time the ball crosses the tennis net towards the opponent side, a player gets a reward of +0.1, and if the ball hits the ground or moves outside of the court, the reward is -0.01. Therefore, a player should play well to pass a ball towards the other player to get a chance of high score.

Each player's observation/state space has 24 dimensions consisting of 8-dimensional states stacked over 3 time steps. It contains the player(racket) and ball's position and velocity. Given this information for both players, the agent has to learn how to move each player/racket properly to hit a ball. Two continuous actions are available with the range of [-1, 1]. The first action value controls the movement and the second makes a player jump.

Because there are 2 players in a **Tennis** game, 2 x 24 observations are given in each time step and the agent needs to make an action for both players which requires 2 x 2 action matrix. The codes in the notebook will train an agent to achieve an 100-episode average winner(max of agents) score of +0.5 by using DDPG algorithm.


## Getting Started

#### Requirements
- Linux OS
- Python environment
- [Unity Tennis environment](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
- Git

#### Steps

1. Install Git and Anaconda

2. Create Python environment on Anaconda
```
conda create --name drl python=3.6
conda activate drl
```

3. Clone the the following repository and install Python dependencies to run the code
```
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
pip install .
```

4. Create IPykernel to use the current environment
```
python -m ipykernel install --user --name drl --display-name "drl"
```

5. Download the following Linux Unity environment zip archive file.
    - [Unity Tennis environment](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)

6. Place the file in the current root folder of this repository, and unzip (or decompress) the file. 

7. Run Jupyter/Ipython Notebook and Change the kernel to "drl"

8. Make Unity Environment to point to the file decompressed by the step 5
```
env = UnityEnvironment(file_name="./Tennis_Linux/Tennis.x86_64")
```

9. Follow the steps in the notebook `Tennis.ipynb` from top to bottom.


## Instructions

All the codes (Model, Training and Simulation) are written in `Tennis.ipynb`. Please follow the notebook from top to bottom to create, train and test the agent.
It can be directly modified for any changes of the algorithm inside a notebook
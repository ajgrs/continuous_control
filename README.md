#Udacity Deep Reinforcement Learning Nanodegree
  
##Continuous Control

1.	Project Description

The current project attempts to solve a continuous learning task using a model-free off-policy deep reinforcement learning algorithm called DDPG – Deep Deterministic Policy Gradient, (Lillicrap et. all, "Continuous control with deep reinforcement learning", 2016) that extends the work on Deterministic Policy Gradient algorithm (Silver et al., 2014) using recent successes from Deep Q-Learning (Mnih et al., 2013; 2015) and uses an actor and a critic neural network to decide on which actions to take and evaluate them, respectively.

The task consists of a double-jointed arm controlled by the agent that must learn how to move the arm to target locations produced by the environment. The environment provides a reward of +0.1 at each time-step if the agent is capable of keeping the arm’s hand at a target location.

The goal of the agent is therefore to maintain the arm’s hand at the target location at all times during all time-steps in a given episode so as to maximise its total reward.

2.	Environment

An adapted version of the Reacher environment is used in the project. Observation states are composed of 33 variables which correspond to physical quantities such as the double-jointed arm’s position, rotation, velocity and angular velocities of each joint. Each variable is a number between -1 and 1.

The action space is composed of a vector with 4 continuous variables which correspond to the torque applicable to each of the harm’s joints. Each variable is a real number between -1 and 1.

In our project we have focused on the 20-agents’ version of the adapted Reacher environment. This environment’s version accepts a matrix of 20 different actions and returns 20 different rewards, 20 next observation states and a set of 20 episode-conclusion flags, one for each environment instance respectively.

Using the 20-agents’ version, the task is considered solved when the average score obtained across all 20 environment instances is greater than 30 over 100 consecutive episodes.

3. Implementation

Our implementation uses makes use of two neural networks called actor and critic which we train to to learn a mapping from states provided by the environment and the best continuous action values. The actor is trying to learn about the best actions to take while the critic learning to evaluate those actions.

4. To run the code simply download the available files to a folder, open the Jupyter Notebook and select "Kernel -> Restart & Run All".

5. Dependencies
Python 3.6, Numpy 1.15.1, Pytorch 0.4.0, UnityEnvironment.

6. Credits
The baseline implementation of the DDPG algorithm was taken from here https://github.com/higgsfield/RL-Adventure-2. It was so elegantly implemented that we just had to use it as our first try in cracking the Reacher environment :-)

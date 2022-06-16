---
layout: post
title: Automating Flappy Bird using Deep Q-learning
date: 2021-07-06 
description: Automating Flappy Bird using Deep Q-learning. 
---

Codes and reports can be seen [here](https://github.com/huacailong/Automating-Flappy-Bird-using-Deep-Q-learning).


# Automating Flappy Bird using Deep Q-learning
Here, we want to design an agent that can automate the flappy bird game based on state vectors instead of images, where the flappy Bird is a game that involves navigating a bird through a bunch of obstacles using reinforcement learning without knowing any information from the environment apriori.

Based on the rewards received, the agent learns to behave in a given environment under certain policy. Reinforcement Learning is mainly concerned with the maximization of cumulative reward in return to the agent-environment interaction. Deep Q-Learning is an advanced version of Q-Learning method of Reinforcement Learning where deep neural networks are used to solve Reinforcement Learning problems.

We attempted to automate the game flappy bird without giving the agent any environment related information except for rewards that it gets for different actions. The action value function was represented using a neural network and the network was trained using deep Q learning algorithm to store the Q values. Besides, we found out that our vector-based learning for flappy bird game is a little bit faster than the image-based one, which may give the intuition that we may decrease the information contained in the image further to get a better training speed since the image is constituted with vectors. So if we can find a proper method to do pre-processing on the image to keep the necessary information before training, we will have a better learning speed, and this is the work we want to study in details in the future.


## gym-simpleflappy
A Gym environment for a Flappy bird clone with a simple observation space.

Observations returned are:
```
[bird height, bird speed, distance to next pipe, height of next pipe, distance to second pipe, height of second pipe]
```

Use `gym.make("SimpleFlappy-v0")` for rewards only when a pipe is passed.

Use `gym.make("SimpleFlappyDistance-v0")` for rewards based on steps survived - less sparse rewards should make the task a bit easier.


## Run an Example

Run this sample agent ("flappy_random_agent.py")to see the environment in action

This agent picks a random action (flap or not flap) every 15 frames. Score is printed after each episode. 


## Run the trained agent

Run the file "dqn_vector_flappyBird_final.py" to test the agent with pre-trained model. 


## Test video

A short test video is shown in "Test.MP4", where the agent has scored more than 1500. 


## Score and Q(s,a)

These values are stored in "Q.txt" and "S.txt" for the last training. 


## Pretrained model

The pretrained model is saved in the folder "pretrained_model_vector"

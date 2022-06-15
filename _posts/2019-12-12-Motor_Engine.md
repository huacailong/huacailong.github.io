---
layout: post
title: Molecular Motor Engine
date: 2019-12-12
description: Stochastic Models for Intra-cellular Cargo Transport.
---

### Overall Goal:
- To model the cargo transport process as a combination of free diffusion and motor based transport
- Obtain time-evolution of the position and velocity of the cargo
- Get biologically relevant statistics using position and velocity evolution

### Approach:
- Computational: Approximate numererical solutions to SDEs (e.g. Euler-Maruyama)
- Semi-Analytical: Use closed form solutions for each (sub)regime, combine them for faster computational solution
- Analytical: Attempt to find analytical solution to the joint SDEs with Poisson jumps and regime switching

The code can be found [here](https://github.com/huacailong/Molecular-Motor-Engine).

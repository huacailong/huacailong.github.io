---
layout: post
title: UMN Projects
date: 2019-12-12
description: Projects at University of Minnesota
---

# Stochastic Models for Intra-cellular Cargo Transport (2019)
### Overall Goal:
- To model the cargo transport process as a combination of free diffusion and motor based transport
- Obtain time-evolution of the position and velocity of the cargo
- Get biologically relevant statistics using position and velocity evolution

### Approach:
- Computational: Approximate numererical solutions to SDEs (e.g. Euler-Maruyama)
- Semi-Analytical: Use closed form solutions for each (sub)regime, combine them for faster computational solution
- Analytical: Attempt to find analytical solution to the joint SDEs with Poisson jumps and regime switching

The code can be found [here](https://github.com/huacailong/Molecular-Motor-Engine).


# Robust control for Self-erecting Inverted Pendulum (SESIP) (2020)
Codes and reports can be seen [here](https://github.com/huacailong/Robust-Control-of-SESIP).

The self-erecting single inverted pendulum (SESIP) is an unstable, multi-variable and fourth order system. We focus on the stabilizing and tracking control in this project. 

In this project, the SESIP model is introduced first, then LQR control is applied with tracking the predetermined trajectory, stabilizing the inverted pendulum vertically and maintaining the input signal u(t) within 10V. Then we analyze LQR control with real uncertainty and multiplicative uncertainty. Last, we use H∞ and μ-synthesis control to further analyze the robustness and performance characteristics of the system.

First, we implemented the double PID control, while the double PID control is not good to use. Therefore we change to the LQR control, we first use simple LQR, but the input signal is too large, which exceeds our limitation. Due to this reason, we add extra weighting term on our input signal.

Then, we test the robust stability of controller with real uncertainty and dynamic uncertainty. And we can conclude that LQR control has a very good robustness on real uncertainties, but it has a weak robustness on multiplicative uncertainty. Besides, we found that the LQR control without limitation on u(t) will give stronger robustness on multiplicative uncertainty compared with LQR with limitation on u(t). It’s probably because limitation on u(t) gives up some robust stability and we need to clarify it in the future.

Last, we move to H∞ and μ-synthesis control to get a more robust controller based on the multiplicative uncertainty and try to do model reduction on kμ to make it more applicable in the real world. However, we don’t go deep in the model reduction method here, and it’s still unclear why the reduced controller with order 11 will give lower bound 0, which needs future work as well.

- Please see more details in "Robust control for Self-erecting Inverted Pendulum.pdf"
- Codes and how to use them can be seen in "Pendulum_lqr.pdf", "pendulum_hinf.pdf" and "pendulum_uncertainty.pdf" 


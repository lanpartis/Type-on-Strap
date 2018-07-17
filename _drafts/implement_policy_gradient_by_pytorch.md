---
layout: post
title: Implement Policy Gradient by Pytorch
categories:
  - Reinforcement Learning
tags:
  - [Reinforcement Learning, Policy Gradient]
---

#Problem definition

target function:
$$ \max_\theta L(\theta)=\sum\log\pi(a\|s,\theta)r(s,a)$$

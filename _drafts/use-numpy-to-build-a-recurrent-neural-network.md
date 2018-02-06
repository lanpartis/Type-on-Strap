---
layout: post
title: Use numpy to build recurrent neural networks
category: Deep Learning
tags: [Numpy, RNN]
---
Though we can directly use RNN modules from deep learning libraries such as Keras, Pytorch, it is still worth your effort to do with these tensor calculations in detail. By doing so we strength our understanding of its forward/backward propagation. We will find this experience very useful when we start to construct DNNs, to play with hyperparameters or troubleshooting.

This tutorial is basically following Andrew NG's online course **Sequence Models** on coursera.

## 1.1 RNN cell

A Recurrent neural network can be seen as the repetition of a single RNN cell. The first thing we need to implement is the one time-step forward computation.

The RNN cell looks like this.
![pic](/assets/postfiles/imgs/rnn_step_forward.png)

Here's the code:
``` python
import numpy as np

def softmax(X):
    e_x = np.exp(x - np.max(X))
    return e_x/e_x.sum(axis=0)

def rnn_cell_forward(xt, a_prev, parameters):

    Wax = parameters["Wax"]
    Waa = parameters["Waa"]
    Wya = parameters["Wya"]
    ba = parameters["ba"]
    by = parameters["by"]

    a_next = np.tanh(np.dot(Wax,xt) + np.dot(Waa,a_prev) + ba)
    yt_pred = softmax(np.dot(Wya,a_next)+by)  
    # store values you need for backward propagation in cache
    cache = (a_next, a_prev, xt, parameters)  

    return a_next, yt_pred, cache
```
## 1.2 Rnn forward pass

```python

```

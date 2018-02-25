---
layout: post
title: Neural Style Transfer with Pytorch
category: Deep Learning
tags: [Style Transfer, Pytorch]
---
The Neural-Style, or Neural-Transfer, is an algorithm that takes as
input a content-image, a style-image and return the content of the content-image as if it was
'painted' using the artistic style of the style-image.

To change the style while keeping the original content, two Distances of style ($$D_s$$) and content ($$D_c$$) are defined. ($$D_s$$) measures how different the style between two images, ($$D_c$$) measures how different the content between two images.

Let $$C_{nn}$$ be a
pre-trained deep convolutional neural network and $$X$$ be any
image. $$C_{nn}(X)$$ is the network fed by $$X$$ (containing
feature maps at all layers). Let $$F_{XL} \in C_{nn}(X)$$ be the
feature maps at depth layer $$L$$, all vectorized and concatenated
in one single vector. We simply define the content of $$X$$ at layer
$$L$$ by $$F_{XL}$$. Then, if $$Y$$ is another image of same
the size than $$X$$, we define the distance of content at layer
$L$ as follow:

$$D_C^L(X,Y) = \|F_{XL} - F_{YL}\|^2 = \sum_i (F_{XL}(i) - F_{YL}(i))^2$$






Reference:

Pytorch tutorial of Neural Transfer

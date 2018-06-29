---
layout: post
title: Skeleton Based Interaction Recognition
feature-img: "assets/img/portfolio/submarine.png"
img: "assets/img/portfolio/submarine.png"
date: 2017-10-15
---

## Motivation
To let robots learn Human Robot Interaction, I believe it is necessary to make robot understand interactions first. In our [previous research](https://arxiv.org/pdf/1702.07492.pdf), robot start to learn to interact with people totally based on camera informations, which limited the capability of the robot to learn more complex interactions.

Also, it's obvious that skeleton key points contain far more dense informations of human actions than raw images. So ,with many state of the art researches that make it easy to obtain skeleton informations, I think we can build a skeleton based interaction classifier to help robot understand what are people doing and respond according to recognition result.

## Data collection

To collect natural interaction data, we gathered 12 subjects to let them watch some videos and talk about the contents. During their conversation we recoded the interaction video by one omnidirectional camera.

After acquiring this dataset we manually labeled the short clips of video datas into 7 interaction labels, meanwhile we also kept those
interaction clips that cannot be labeled into words as one category `unknown interaction'.
Moreover, As shown below, we used Openpose to extract the skeleton key points from videos.

![](/assets/postfiles/imgs/demo_rgb.png)

## Data augmentation
Data augmentation is a famous method to train robust models, especially in image classification. In this work, since we are dealing with the skeleton data as images, we also do data augmentations such as random clipping(in temporal axis) and Fliping (in spatial axis)
## Algorithm

Sequential data is typically dealt with Recurrent Neural Networks, many skeleton based action recognition works are done with RNNs and have good results.
However, Bai et al. found Convolutional Neural Networks are also good at sequence modeling or even better. Moreover, Li et al.\cite{li2018} use CNNs for action recognition and archived state of the art accuracy.

In this work, we also use CNNs to deal with the sequential skeleton data.

## Model
![](/assets/postfiles/imgs/model.PNG)

The first fully connected layer is crucial since it helps each convolution kernel to obtain relations between key points that are far away, such as right wrist and left foot, which can be a determinant feature for punching.
## Result

![](/assets/postfiles/imgs/res_table.png)

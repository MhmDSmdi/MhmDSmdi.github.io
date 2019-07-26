---
title: 'Why Autoencoder?'
date: 2019-07-26
permalink: /posts/2019/07/autoencoder/
tags:
  - Autoencoder
  - DeepLearning
---



## Introduction
**Autoencoder** is an neural network which aims to copy its input to its output. It uses unsupervised-learning technique to reconstruct the output it means we don't have any labels. As is clear, "Autoencoder" consist of 2 parts : 'Auto' + 'Encoder' so it related to an encoder which encodes data. 

## Autoencoder Architecture
At first I explain the simplest architecture which has just one hidden layer. It has two main parts: 
1. An encoder which encode input to a **latent space representation** (dimension reduction) 
2. A dicoder to convert latent space representaion to output which idealy is equal to the input.
![alt text](https://raw.githubusercontent.com/MhmDSmdi/mhmdsmdi.github.io/master/images/autoencoder.png)
For example, the figure above is a simple autoencoder which has one hidden layer in order to encode 10d feature space to 4d latent space.

Like other neural network and machine learning model we need to define a cost function (loss function) to minimize the model's error to increase the similarity of input and output. This cost function measure how much the input and the output are different (even it might measure the similarity of input and output). Hence with this function the autoencoder is forced to learn the latent space presentation as good as possible.

But why 

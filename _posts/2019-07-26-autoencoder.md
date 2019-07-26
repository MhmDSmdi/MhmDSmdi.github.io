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
For example, the figure above is a simple autoencoder which has one hidden layer in order to encode 10 dimensions feature space to 4 dimensions latent space.

Like other neural network and machine learning model we need to define a cost function (loss function) to minimize the model's error to increase the similarity of input and output. This cost function measure how much the input and the output are different (even it might measure the similarity of input and output). Hence with this function the autoencoder is forced to learn the latent space presentation as good as possible.

***But what should it copy the input to the output?***

To answer this question, first we should get to know **Dimension Reduction** which is the process to reducing the dimensions of   random variables under considerations by capturing a set of principal variable. It is an effective technique to reduce the time and storage space.

As mentioned befor autoencoder encodes the input to latent space which has useful properties and is the essential part of autoencoder. Because after training, this latent space representation can be connected to a multilayer perceptron (MLP) or any deep networks. The decoder attempts to re-construct the input from latent space representation and that's the point! In this senario autoencoder is forced to convert latent space to the output without paying attention to input. Because of that it should copy the input to the output.
![alt text](https://raw.githubusercontent.com/udacity/deep-learning/c6b46a0bfcb8d4afcb806174b3923d3ea89ca455/autoencoder/assets/autoencoder_1.png)
[Source](https://raw.githubusercontent.com/udacity/deep-learning/c6b46a0bfcb8d4afcb806174b3923d3ea89ca455/autoencoder/assets/autoencoder_1.png)

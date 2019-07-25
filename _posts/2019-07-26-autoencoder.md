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
At first I explain the simplest architecture which has just one hidden layer. It has two main parts: 1) an encoder which encode input to a latent space representation (dimension reduction) 2) a dicoder to convert latent space representaion to output which idealy is equal to the input.

![alt text](https://raw.githubusercontent.com/MhmDSmdi/mhmdsmdi.github.io/master/images/autoencoder.png)


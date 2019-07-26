---
title: 'Part1 : What is Autoencoder?'
date: 2019-07-26
permalink: /posts/2019/07/autoencoder/
tags:
  - Autoencoder
  - DeepLearning
---



## Introduction
**Autoencoder** is a neural network which aims to copy its input to its output. It uses an unsupervised-learning technique to reconstruct the output it means we don't have any labels. As is clear, "Autoencoder" consists of 2 parts: 'Auto' + 'Encoder' so it is related to an encoder which encodes input to a mysterious code. It has following types that have different architecture:
* Vanilla autoencoder
* Multilayer autoencoder
* Convolutional autoencoder
* Regularized autoencoder

## Autoencoder Architecture
At first, I explain the simplest architecture (Vanilla autoencoder) which has just one hidden layer. It has two main parts: 
1. An encoder which encodes input to a **latent space representation** (dimension reduction). it acts as a function like h = f(x) that code the input(x).
2. A decoder to convert latent space representation to output which ideally is equal to the input but usually(If an autoencoder succeeds in simply learning to set everywhere, then it is not useful). it is a function to re-construct input x' = g(f(x)).

![alt text](https://raw.githubusercontent.com/MhmDSmdi/mhmdsmdi.github.io/master/images/autoencoder.png)

For example, the figure above is a simple autoencoder which has one hidden layer to encode 10 dimensions feature space to 4 dimensions latent space.

Like other neural network and machine learning model, we need to define a cost function (loss function) to minimize the model's error to increase the similarity of input and output. This cost function measure how much the input and the output are different (even it might measure the similarity of input and output). Hence with this function, the autoencoder is forced to learn the latent space presentation as good as possible.

***But what should it copy the input to the output?***

To answer this question, we should get to know **Dimension Reduction** which is the process of reducing the dimensions of random variables under considerations by capturing a set of principal variable. It is an effective technique to reduce the time and storage space.

![alt text](https://raw.githubusercontent.com/MhmDSmdi/mhmdsmdi.github.io/master/images/autoencoder_1.png)

As mentioned before autoencoder encodes the input to latent space which has useful properties and is the essential part of the autoencoder. Because after training, this latent space representation can be connected to a multilayer perceptron (MLP) or any deep networks. The decoder attempts to reconstruct the input from latent space representation and that's the point! In this scenario autoencoder is forced to convert latent space to the output without paying attention to input. Because of that, it should copy the input to the output with a little loss.

## Getting started with Keras
In the following codes, used Keras and python to implement autoencoder using MNIST dataset.

### Vanilla autoencoder
At first we should load dataset (train and test). Because the range of data is 0 - 255, normalized between 0 - 1 by deviding 255.
``` python
encoding_dimension = 32
input_dimension = 28 * 28
(x_train, _), (x_test, _) = mnist.load_data()
x_train = x_train.astype('float32') / 255.
x_test = x_test.astype('float32') / 255.
x_train = x_train.reshape((len(x_train), np.prod(x_train.shape[1:])))
x_test = x_test.reshape((len(x_test), np.prod(x_test.shape[1:])))
```

After that, Vanilla autoencoder is constructed by 3 Dense layer (input-code-output).
``` python
input_image = Input(shape=(input_dimension,))
encode = Dense(encoding_dimension, activation='relu')(input_image)
decode = Dense(input_dimension, activation='sigmoid')(encode)
autoencoder = Model(input_image, decode)
encoder = Model(input_image, encode)
encoded_input = Input(shape=(encoding_dimension,))
decoder_layer = autoencoder.layers[-1]
decoder = Model(encoded_input, decoder_layer(encoded_input))
```
And Finally, fit and compile our model:
``` python
autoencoder.compile(optimizer='adadelta', loss='binary_crossentropy')

autoencoder.fit(x_train, x_train,
                epochs=50,
                batch_size=256,
                shuffle=True,
                validation_data=(x_test, x_test))
```

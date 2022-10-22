---
layout: post
tags: ["pytorch","Machine Learning", "IEEE"]
title: "Neural Networks with PyTorch Workshop"
date: 2020-10-15T20:46:10-07:00
math: false
draft: false
---
[Github
Repository](https://gitlab.com/deep-learning-for-all/deep-learning-part-1/-/tree/master)

For my first workshop for the IEEE@UCI, I wanted to talk about something I found
interesting, so I decided to do a workshop on neural networks. Because of its
recently growing popularity, most engineering students have heard of neural
networks, even if they don't necessarily understand how they work.

My goal with this workshop was to both introduce people to the math behind
neural networks and to let people have hands-on practice composing and training
a neural network.

This workshop covers the following information:
* Forward Propagation as matrix multiplication
* Activation functions as nonlinearities (ReLU, Sigmoid, tanh)
* Loss functions and model evaluation (MSE, maximum likelihood)
* Backpropagations and calculating gradients
* Convolution layers
* Constructing a custom model class in PyTorch
* Training and inference on the MNIST Dataset of handwritten digits
* Saving model weights and loading pre-trained weighted

Participants had the option of following along with the MNIST example, either
in their own Python file or on a Google Colab Notebook:

[Python
Template](https://gitlab.com/deep-learning-part-1/-/blob/master/mnist_final.py)

{{<gslides src="https://docs.google.com/presentation/d/15NaS0GNFvyRBaD-FSeqc8TCUV1OUI0oBzzBA3TKUAOQ/embed?start=false&loop=false&delayms=3000">}}
---
layout: post
tags: ["LLNL","Machine Learning", "internship"]
title: "Machine Learning Internship @ LLNL"
date: 2021-11-20T20:46:33-07:00
math: false
draft: true
---

My second summer internship at Lawrence Livermore National Laboratory (LLNL)
focused on comparing machine learning inference performance on novel AI hardware
accelerators from Samba Nova and Cerebras to NVIDIA GPUs. I was working with a
autoencoder model used to material interface reconstruction (MIR) for
multi-material hydrodynamics codes. The neural network was proposed as an
alternative to current solution PLIC: the neural network provided much smoother,
continuous boundaries than PLIC, which could only give linear approximations.
However, in order for the neural network to be a replacement for PLIC, it would
need to have at least as good of a throughput as PLIC, which is around 100,000
samples a second.

The original model comprised of 5 convolutional layers, each with 32 channels,
leading to a fully connected layer of size 131072. Then after some fully
connected layers, there were 5 deconvolution layers, each with 32 channels. The
inputs and outputs of the models were 64x64 images. Since the number of
parameters in the model was large and the size of the inputs was also large, as
the size of the mini-batch increased, running the model on a single GPU quickly
ran into memory problems. Similarly, there were problems running the model on
Samba Nova's hardware. In order to fix this, I shrank the size of the model by
decreasing the number of convolution channels and adding pooling layers after
every convolution/deconvolution layer for additional downsampling. I did a sweep
over different combinations of the number of convolution channels, pooling
stride and dilation, and found that a model with pooling and 2 convolution
channels had the best performance and even out-performed the original model. It
also, on NVIDIA A100 GPUs and the Samba Nova SN-10 hardware, did exceed the
target throughput of 100,000 samples per second.



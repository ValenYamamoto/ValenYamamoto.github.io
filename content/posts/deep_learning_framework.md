---
layout: post
tags: ["Machine Learning","C++"]
title: "Deep Learning Framework in C++"
date: 2020-12-08T17:38:57-07:00
math: false
draft: false
---

[Github Repository](https://github.com/ValenYamamoto/DeepLearningFramework)

Ever since I started learning PyTorch, I have been fascinated by the automatic
gradient feature. In order to further understand it, I decided I would try to
write my own version. At the time, I was also taking a C++ class, so I decided
to both learn about autograd and study for my finals. (As well as do the
required project to initiate into IEEE-HKN)

This program dynamically constructs a computation graph as operations are done.
When the backward function is called on the final node, then, just as in
PyTorch, all the gradients are calculated for all the intermediate nodes. 

Currently, this program only supports linear layers. For non-linear activation
functions, the program requires that both the function and a function for its
derivative/gradient are passed in. I included a Sequential wrapper, which does
exactly what it does in PyTorch. Even those I wrote these layer abstraction, the
automatic differentiation still works for math done outside layers.

The current mathematical operations this program supports are:
* Elementwise addition, subtraction, mulitplication
* Matrix multiplication
* Reduce sum

Because I also did this project to strengthen my C++ skills, this project tries
to knock off most of the basic, object-oriented C++ skills:
* Classes - All layers and tensors are implemented as classes, as well as my SGD
  implementation
* Polymorphism and Inheritence - Layer classes all descend from an abstract base
  class and overload the forward method, just as they do in PyTorch
* Operator Overloading - Since the dynamic computation graph is built as
  operations are done on tensors, I have overloaded the basic operators
  (+,-,\*,/) to add to the graph when executed
* Functions and Lambdas - Activation functions and their derivatives need to be passed
  in when being used, and they can either be written traditionally as a function
  or as a lamdba function

This project also gave me the opportunity to practice other coding related
skills, including:
* Makefiles - I wrote my own Makefile for this project to compile both
  executables and intermediate object files
* Memory Check - I used valgrind to check for memory leaks and uninitialized
  memory reads


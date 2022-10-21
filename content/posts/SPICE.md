---
layout: post
tags: ["python","SPICE", "IEEE"]
title: "Python Scripts for Parsing SPICE Output: A Workshop"
date: 2021-04-23T20:46:17-07:00
math: false
draft: false
---
[Github Repository](https://github.com/ValenYamamoto/IEEE_Python_Workshop)

Python is particularly useful for writing quick scripts. I find myself reaching
for Python whenever I need to parse output into more readable/processable forms
like csv files or pandas DataFrames. Engineering students at UCI don't spend a
lot of time learning Python, so I thought this would be a particularly useful
exercise.

This workshop goes through a program to parse PSPICE output and allows the user
to either output a csv version of the output or to pick out particular
components with voltages or currents above a specified threshold. This program
was originally written to parse the provided output for components with a
voltage greater than 3.6 V, indicating a breakdown voltage.

The input to the program is a threshold voltage or current and a SPICE output
file, which looks something like this:

![SPICE Output](/images/spice_output.png)

The output is printed to the terminal in csv format. 

![SPICE CSV](/images/spice_csv.png)

The key Python concepts covered in this workshop are as follows:
* Reading files and iterating over files as generators
* Splitting, concatenating, and regex for strings
* f-strings for formatting output
* argparse for including command line options

A Google Colab template for participants to follow along with can be found at
the following:
* [Python Template](https://colab.research.google.com/drive/1SW3-krotbXJKfcejoYD3OCpK_Mn2YIXJ?usp=sharing)

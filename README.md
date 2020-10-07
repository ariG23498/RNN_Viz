# How do the sequence models work?

### Introduction

The code-base contains `Numpy` implementations of two sequence model architectures, a vanilla `Recurrent Neural Network` and a vanilla `Long Short Term Memory`. This repository is for those who want to know what happens under the hood of these architectures.

In the repository care is given to the `feed-froward` and `back-propagation` of the architectures. The derivations are unrolled as much as I could to make it understandable.

The goal is to tackle the problem of `character generation` using RNNs and LSTMs. While tackling the problem, we also look into the gradient flow of the architectures. Later on an experiment to show the `context understanding` is done too.

### Problem Statement

The input will be a sequence of characters and the output would be the immediate next character in the sequence. The image below demonstrates the approach. The characters in a particular sequence are `H, E, L, L` and the next character is `O`. A little thing to notice here is that the character `O` could have been a `,` or simply a `\n`. The character that is generated largely depends on the context of the sequence. A well-trained model would generate characters that fit the context very well.

![Problem.png](https://api.wandb.ai/files/authors/images/projects/126026/643ae901.png)



### Feedforward

We look into the recurrence formula for both the architectures.

![Recurrence RNN](https://api.wandb.ai/files/authors/images/projects/126026/982cd0e9.png)

<center>Recurrence formula of RNN</center>

![Recurrence LSTM](https://api.wandb.ai/files/authors/images/projects/126026/d8dc8d9d.png)

<center>Recurrence formula of LSTM</center>

### Backpropagation

We look into the backpropagation formula for both the architectures.

![Back RNN GIF](https://api.wandb.ai/files/authors/images/projects/126026/f27234c0.gif)

<center>Backpropagation in RNN</center>

![Back LSTM GIF](https://api.wandb.ai/files/authors/images/projects/126026/72f4f51e.gif)

<center>Backpropagation in RNN</center>


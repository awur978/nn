<img src="https://github.com/coledd/nn/blob/master/logo.png" width="300">

Neural Network library

Copyright (c) 2019 Cole Design and Development, LLC

https://coledd.com

SPDX-License-Identifier: Apache-2.0

## Overview

This is a lightweight neural network library for use in microcontrollers and embedded systems. 

The code is divided into the following sections:

1. `nn.[ch]` - The neural net library, which can be pulled into a project in whole, and should not require modification to use.

2. `train.c` - An example of how to use nn.c to construct, train, and save a neural network model.

3. `test.c` - Evaluates the model performance, comparing that of seen vs. unseen data.

4. `predict.c` - Demonstrates how to use a saved neural network model in the target application to make predictions on new data.

## Features

With this library, neural networks of any width and depth may be constructed and trained. The following activation functions are supported:

* Identity
* Linear
* ReLU
* Leaky ReLU
* ELU
* Threshold
* Sigmoid
* TanH

Different activation functions may be assigned to each layer in the network.

A bias can be added to each layer independently.

## Instructions

To build the nn library and sample training and prediction programs, just type:
```
make
```


To train:
```
./train
```
The included example data is the Semeion Handwritten Digit Data Set from the UCI Machine Learning Repository at:

http://archive.ics.uci.edu/ml/datasets/semeion+handwritten+digit


To evaluate the model performance:
```
./test
```


To use the trained model:
```
./predict
```

## Architecture

The network architecture is a fully connected feed-forward neural network. The widths of each layer, the activation function to be used, and the bias for each layer is set as each successive layer is added to the network using the `nn_add_layer()` function call. Multiple layers may be added to construct a deep neural network.

<img src="https://github.com/coledd/nn/blob/master/nn.png" width="600">

(The size and number of layers in a given neural network may vary from the one depicted above)

## Demonstration

This embedded neural network library was used to power a handwritten character recognition application running on an STM32H7 microcontroller. Check it out here:

https://www.youtube.com/watch?v=cqjwSkrGtww

## License

Copyright (c) Cole Design and Development, LLC. All rights reserved.

Licensed under the [Apache License 2.0](./LICENSE).


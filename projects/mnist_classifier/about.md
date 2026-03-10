# MNIST Digit Classifier

## Objective

The goal of this project is to build a neural network that can classify handwritten digits from the MNIST dataset.

MNIST is one of the most widely used benchmark datasets in machine learning.

## Dataset

MNIST contains:

- 60,000 training images
- 10,000 testing images

Each image represents a digit between 0 and 9.

Image size: 28 × 28 pixels.

## Model Architecture

Flatten Layer → Dense(128) → Dense(10)

Activation Functions:

ReLU
Softmax

## Evaluation

The model is trained on the training dataset and evaluated on the test dataset to measure classification accuracy.

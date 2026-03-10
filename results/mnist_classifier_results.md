# MNIST Classifier Results

## Experiment Overview

This experiment trains a neural network to classify handwritten digits using the MNIST dataset.

Dataset:

- Training samples: 60,000
- Test samples: 10,000
- Image size: 28 × 28 pixels
- Number of classes: 10

---

## Model Architecture

Flatten → Dense(128) → Dense(10)

Activation Functions:

- ReLU
- Softmax

Optimizer: Adam
Loss Function: Sparse Categorical Crossentropy

---

## Training Configuration

Epochs: 5
Batch Size: Default (TensorFlow)

---

## Results

Training Accuracy: ~98%
Test Accuracy: ~97%

---

## Observations

The neural network successfully learns to classify handwritten digits with high accuracy.

Even a simple fully connected architecture performs well on MNIST because the dataset is relatively simple.

Future improvements may include:

- Convolutional Neural Networks
- Data augmentation
- Hyperparameter tuning

# TensorFlow Neural Network Experiment

## Objective

The purpose of this experiment was to explore how neural network layers are implemented internally in TensorFlow.

A custom dense layer was created by subclassing `tf.keras.layers.Layer`.

---

## Key Concepts Explored

- Custom layer creation
- Weight initialization
- Forward propagation using TensorFlow operations
- Matrix multiplication using `tf.matmul`

---

## Experiment

A custom dense layer was tested using a simple input vector.

Input:

[1, 2]

The layer computes:

z = Wx + b

Output is produced using the sigmoid activation function.

---

## Observations

The experiment demonstrates how TensorFlow manages parameters such as weights and biases inside a neural network layer.

Understanding this mechanism is important for building custom architectures and debugging models.

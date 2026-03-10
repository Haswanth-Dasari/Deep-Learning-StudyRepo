# Neural Network Basics

## Introduction

A neural network is a computational model inspired by the structure of the human brain. It consists of interconnected processing units called **neurons**, organized into layers. Neural networks are designed to learn patterns from data and approximate complex functions.

Neural networks are widely used in tasks such as:

- Image recognition
- Natural language processing
- Speech recognition
- Recommendation systems
- Time series prediction

The fundamental idea is to transform input data through multiple layers of computation to produce meaningful outputs.

---

# Structure of a Neural Network

A basic neural network consists of three types of layers:

### 1. Input Layer

The input layer receives the raw data and passes it to the network.

Example:

For an image classification problem:

Input = pixel values of the image

If the image is 28×28 pixels, the input layer may contain 784 input features.

---

### 2. Hidden Layers

Hidden layers perform intermediate computations and learn representations of the data.

Each hidden layer consists of multiple neurons that perform:

Linear transformation
followed by
Non-linear activation

Mathematically:

z = Wx + b

Where

W → weight matrix
x → input vector
b → bias vector

The output of this operation is then passed through an **activation function**.

---

### 3. Output Layer

The output layer produces the final prediction.

Examples:

Binary classification → sigmoid activation
Multi-class classification → softmax activation
Regression → linear output

---

# Neuron Computation

Each neuron performs two main steps.

### Linear Transformation

z = Wx + b

Where:

W = learnable weights
x = input
b = bias

---

### Activation Function

a = σ(z)

The activation function introduces **non-linearity**, allowing the network to learn complex patterns.

Without activation functions, the network would behave like a simple linear model.

---

# Common Activation Functions

### ReLU (Rectified Linear Unit)

ReLU(x) = max(0, x)

Advantages:

- Computationally efficient
- Avoids vanishing gradient problem

Widely used in deep learning.

---

### Sigmoid

Sigmoid(x) = 1 / (1 + e^(-x))

Range: (0,1)

Often used for binary classification.

---

### Tanh

tanh(x) = (e^x - e^-x) / (e^x + e^-x)

Range: (-1,1)

Zero-centered activation.

---

# Loss Function

The loss function measures the difference between predicted output and actual output.

Common loss functions:

Mean Squared Error (MSE)

Used for regression tasks.

Cross Entropy Loss

Used for classification problems.

Example for classification:

Loss = - Σ y log(ŷ)

Where

y = true label
ŷ = predicted probability

---

# Training a Neural Network

Training involves adjusting weights and biases to minimize the loss function.

This process involves three main steps.

---

### 1. Forward Propagation

Input data passes through the network layer by layer to generate predictions.

---

### 2. Loss Computation

The predicted output is compared with the true output using a loss function.

---

### 3. Backpropagation

Backpropagation computes gradients of the loss with respect to each parameter using the **chain rule of calculus**.

These gradients indicate how the parameters should change to reduce the loss.

---

# Gradient Descent

Gradient descent is an optimization algorithm used to update model parameters.

Update rule:

W = W − η ∂L/∂W

Where

η = learning rate
L = loss function

Variants of gradient descent include:

- Stochastic Gradient Descent (SGD)
- Adam optimizer
- RMSProp

---

# Example Neural Network Architecture

Input Layer → Dense Layer → Activation → Dense Layer → Output

Example:

784 → Dense(128) → ReLU → Dense(10) → Softmax

This architecture is commonly used for the MNIST digit classification task.

---

# Neural Networks in TensorFlow

In TensorFlow, neural networks are typically implemented using:

- `tf.keras.Sequential`
- `tf.keras.layers.Dense`
- custom layer subclasses

Example:

Dense layer:

Dense(units=128, activation="relu")

This automatically creates the weight matrix and bias vector.

---

# Key Takeaways

Neural networks are powerful function approximators capable of learning complex relationships in data. Their effectiveness comes from stacking multiple layers of linear transformations and non-linear activations, enabling the network to learn hierarchical representations of data.

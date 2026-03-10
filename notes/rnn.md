# Recurrent Neural Networks (RNN)

## Introduction

Recurrent Neural Networks (RNNs) are a class of neural networks designed for **sequential data**.

Unlike traditional neural networks, RNNs maintain a **hidden state** that allows them to remember information from previous inputs.

This makes them suitable for tasks where the order of data matters.

Examples of sequential data include:

- text
- speech
- time series
- music
- video frames

---

# Why Standard Neural Networks Are Not Enough

Traditional neural networks assume that inputs are **independent of each other**.

However, in many real-world tasks, context matters.

Example:

Sentence:

"The movie was not good"

Understanding the word **good** requires knowledge of the previous word **not**.

Standard neural networks cannot capture this dependency.

RNNs solve this problem.

---

# Core Idea of RNNs

An RNN processes sequences step by step while maintaining a hidden state.

At each time step:

Input = current element in the sequence
Hidden State = memory of previous inputs

Mathematically:

hₜ = tanh(Wxh xₜ + Whh hₜ₋₁ + b)

Where

xₜ = current input
hₜ = hidden state
hₜ₋₁ = previous hidden state

This recursive structure allows information to flow through time.

---

# RNN Architecture

At each time step:

Input → Hidden State → Output

The hidden state acts as memory that stores information from earlier inputs.

Example sequence:

x₁ → x₂ → x₃ → x₄

Each step updates the hidden state.

---

# Applications of RNNs

RNNs are used in many sequence modeling tasks.

Examples include:

Language Modeling
Predicting the next word in a sentence.

Machine Translation
Translating text from one language to another.

Speech Recognition
Converting speech into text.

Music Generation
Learning patterns in musical sequences.

Time Series Prediction
Forecasting stock prices or weather patterns.

---

# Types of RNN Architectures

### One-to-One

Input → Output

Example:

Image classification.

---

### One-to-Many

Single input produces a sequence of outputs.

Example:

Image captioning.

---

### Many-to-One

Sequence input produces one output.

Example:

Sentiment analysis.

---

### Many-to-Many

Sequence input produces sequence output.

Example:

Machine translation.

---

# Limitations of Basic RNNs

Basic RNNs suffer from the **vanishing gradient problem**.

During training, gradients can become extremely small, preventing the network from learning long-range dependencies.

This limits the ability of simple RNNs to remember information from far earlier in the sequence.

---

# Advanced RNN Architectures

To solve the vanishing gradient problem, more advanced architectures were introduced.

### LSTM (Long Short-Term Memory)

LSTM networks introduce **gates** that control the flow of information.

Gates include:

- Forget gate
- Input gate
- Output gate

These mechanisms allow LSTMs to remember information for long periods.

---

### GRU (Gated Recurrent Unit)

GRU is a simplified version of LSTM.

It combines some gates to reduce computational complexity while maintaining performance.

---

# RNNs in TensorFlow

TensorFlow provides built-in layers for sequence modeling.

Example:

Simple RNN layer:

tf.keras.layers.SimpleRNN(units)

LSTM layer:

tf.keras.layers.LSTM(units)

GRU layer:

tf.keras.layers.GRU(units)

These layers automatically manage hidden states and sequence processing.

---

# Example RNN Model

Example architecture for sequence prediction:

Embedding Layer → RNN Layer → Dense Output Layer

Example in TensorFlow:

Embedding(vocab_size, embedding_dim)
SimpleRNN(units=128)
Dense(vocab_size)

---

# Key Takeaways

Recurrent Neural Networks are specialized neural networks designed to process sequential data. By maintaining a hidden state across time steps, they can capture temporal dependencies in sequences. Although basic RNNs struggle with long-term dependencies, advanced architectures such as LSTMs and GRUs significantly improve sequence modeling performance.

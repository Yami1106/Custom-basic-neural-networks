# 🔢 Simple Neural Network Projects – Binary and Decimal Mappings

This repository contains two custom-built neural network implementations from scratch using only NumPy. Each network solves a specific learning task involving binary inputs and either binary or decimal outputs. No machine learning libraries like TensorFlow or PyTorch are used — all operations, including feedforward and backpropagation, are implemented manually.

---

## 🧠 Problem Statement 1: Predicting 4-Bit Binary Output from 4-Bit Binary Input

**Objective:**  
Design a neural network that takes a 4-bit binary number as input and learns to predict another 4-bit binary number as output. The input–output mappings are arbitrary and nonlinear, representing a transformation function the network must learn.

### Approach:
- Input: 10 random 4-bit binary numbers
- Output: Corresponding 4-bit binary values
- Architecture: 4 layers (including 3 hidden layers with sigmoid activations)
- Output: Sigmoid layer producing values in (0,1), then rounded to binary
- Loss: Binary cross-entropy loss
- Manual backpropagation logic implemented for each layer
- Output compared bitwise with actual output to calculate accuracy

---

## 🔢 Problem Statement 2: Predicting Decimal Output from 4-Bit Binary Input

**Objective:**  
Create a neural network that maps a 4-bit binary input to a single decimal value between 0 and 15. This simulates tasks like digit recognition or regression based on small input vectors.

### Approach:
- Input: 10 samples of 4-bit binary numbers
- Output: A single decimal value (scaled to [0,1] by dividing by 15)
- Architecture: Same 4-layer architecture with sigmoid activation
- Loss: Mean squared error (MSE)
- Prediction: Output scaled back to range [0–15], then rounded to nearest integer
- Accuracy calculated based on exact match and near-match (±1) metrics

---

## 🔧 What's Implemented:
- Weight and bias initialization
- Feedforward for multi-layer perceptron
- Backpropagation for each layer manually coded
- Cost functions: Binary cross-entropy & mean squared error
- Accuracy tracking and prediction display
---

## Problem 3: XOR Gate Learner (Binary Classification)

### 🧠 Problem Statement:
Build a manual neural network from scratch to learn the XOR gate logic using only NumPy. The XOR gate is a classic example of a problem that is **not linearly separable** and therefore cannot be solved by a single-layer perceptron. Your goal is to demonstrate how a multi-layer neural network can successfully model this logic using backpropagation and sigmoid activation.

### 🛠️ Approach:
- Constructed a simple neural network using NumPy arrays for weights and biases.
- Used two binary inputs representing the logic gate values (0 or 1).
- Designed the dataset to include **20 samples** with repeated XOR patterns for better training.
- Implemented:
  - Feedforward computation using sigmoid activations.
  - Backpropagation logic manually across all layers.
  - Training using mean squared error loss.
- Evaluated accuracy by comparing predicted outputs with actual XOR values.

### 📊 Input Format:
Each input is a 2D binary vector `[A, B]` representing the two inputs of the XOR gate.

### ✅ Expected Output:
The output is a binary value (0 or 1) indicating the result of `A XOR B`.

### 📎 Example:
| A | B | A XOR B |
|---|---|---------|
| 0 | 0 |   0     |
| 0 | 1 |   1     |
| 1 | 0 |   1     |
| 1 | 1 |   0     |

This project showcases how neural networks solve non-linear problems when handcrafted from scratch — great for understanding the math behind training!


## 📌 Notes:
- They are **not optimized for production** or large-scale data.
- These projects illustrate the core logic behind deep learning: matrix ops, activations, loss, and gradient descent.

---

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

## 📌 Notes:
- They are **not optimized for production** or large-scale data.
- These projects illustrate the core logic behind deep learning: matrix ops, activations, loss, and gradient descent.

---

# Generalization in Overparameterized Neural Networks

Experiments investigating why highly overparameterized neural networks can generalize well despite having sufficient capacity to memorize training data.

## Research Question

Why can highly overparameterized deep neural networks generalize well despite having enough capacity to fit or memorize their training data?

## Experiments

### 1. Model Scaling
Investigates how increasing model width and parameter count affects training performance and generalization.

### 2. Interpolation and Double Descent
Investigates whether increasing model capacity reaches the interpolation threshold and whether double-descent behavior appears.

### 3. Random-Label Memorization
Investigates whether an overparameterized network can memorize randomly assigned labels and how this depends on the optimization procedure.

This experiment contains three configurations:
- SGD, 30 epochs
- SGD, 100 epochs
- Adam, 100 epochs

### 4. Optimization
Compares SGD and Adam to investigate whether the optimization algorithm affects the learned solution and its generalization behavior.

### 5. Parameter Norms
Investigates whether parameter count alone describes the complexity of a learned solution by comparing parameter norms between generalizing and memorizing models.

### 6. Random Initialization
Investigates the stability of the observed generalization behavior across different random initializations.

## Dataset

All experiments use the MNIST handwritten digit dataset.

## Model

The experiments use a fully connected multilayer perceptron (MLP) with three hidden layers and ReLU activations. Model width is varied across experiments to study the effects of overparameterization.

## Repository Structure

```text
experiments/
├── 01_model_scaling/
├── 02_interpolation_double_descent/
├── 03_random_label_memorization/
├── 04_optimization/
├── 05_parameter_norms/
└── 06_random_initialization/

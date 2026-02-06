# Fashion MNIST Classification: Neural Network Performance Comparison
# Overview
This project implements and compares three different neural network architectures on the Fashion MNIST dataset, focusing on balancing training speed with classification accuracy. The models use different activation functions and optimizers to demonstrate trade-offs in neural network design.

# Dataset
Fashion MNIST: 70,000 grayscale images (28×28 pixels) across 10 fashion categories

Training set: 60,000 images

Test set: 10,000 images

Classes: T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot

# Models Implemented
1. Model 1: ReLU + Adam
Architecture: 2 hidden layers (128→64 neurons)

Activation: ReLU with Batch Normalization

Optimizer: Adam

Regularization: Dropout (0.2)

2. Model 2: Sigmoid + SGD
Architecture: 2 hidden layers (128→64 neurons)

Activation: Sigmoid with Batch Normalization

Optimizer: SGD with Momentum (0.9) and Nesterov

Learning Rate: 0.1

3. Model 3: Mixed Activations
Architecture: 2 hidden layers (256→128 neurons)

Activation: ReLU → Sigmoid

Optimizer: Adam (lr=0.005)

Regularization: Dropout (0.3, 0.2)

4. Ultra-Fast Model (Bonus)
Architecture: Single hidden layer (64 neurons)

Activation: ReLU

Optimizer: Adam

Purpose: Baseline for minimum viable performance

Key Features
Performance Optimizations
Mixed precision training (FP16) when available

Early stopping to prevent overfitting

Learning rate scheduling

Larger batch sizes (128) for faster convergence

Efficient preprocessing (no unnecessary reshaping)

Evaluation Metrics
Test accuracy and loss

Training time comparison

Validation curves

Prediction visualization

Results
The project evaluates models based on:

Accuracy: Classification performance on test set

Training Time: Speed of model convergence

Loss Convergence: Stability during training

Installation & Usage
Prerequisites
bash
pip install tensorflow numpy pandas matplotlib scikit-learn
Running the Code
python
# Clone and run the main script
python fashion_mnist_comparison.py
Output Files
fashion_mnist_ReLU_Adam.keras

fashion_mnist_Sigmoid_SGD.keras

fashion_mnist_Mixed_Adam.keras

best_fashion_model.keras

ultra_fast_fashion_model.keras

# Results Analysis
The project generates:

Training curves: Accuracy and loss over epochs for all models

Bar charts: Test accuracy and training time comparisons

Sample predictions: Visualizations of correct/incorrect classifications

Performance summary: Statistical comparison of all models

# Technical Highlights
Mixed Precision Training
Uses TensorFlow's mixed precision policy for faster computation on compatible GPUs

Maintains accuracy while speeding up training

Callback Strategies
EarlyStopping: Monitors validation accuracy, restores best weights

ReduceLROnPlateau: Reduces learning rate when validation accuracy plateaus

# Efficient Design
Minimal preprocessing overhead

Optimized batch sizes for memory efficiency

Clean architecture with proper regularization

Usage Scenarios
Educational: Learn about activation functions and optimizer impacts

Benchmarking: Compare neural network architectures

Production: Deploy best model for fashion classification

Optimization: Study speed/accuracy trade-offs

# Future Enhancements
Architecture Exploration: Add CNN models for comparison

Hyperparameter Tuning: Grid search for optimal parameters

Deployment: Convert to TensorFlow Lite for mobile

Quantization: Implement 8-bit quantization for edge devices

# Performance Tips Included
The code includes recommendations for:

Using Google Colab with GPU/TPU

Memory optimization techniques

Model simplification strategies

Deployment optimizations

License
This project is open-source and available for educational and research purposes.

Author: Machine Learning Practitioner
Date: 2024
Framework: TensorFlow 2.x
Dataset: Fashion MNIST (Zalando Research)


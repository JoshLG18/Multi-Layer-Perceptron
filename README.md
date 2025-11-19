# Multilayer Perceptron (MLP) for FashionMNIST: A Comparative Study

## Project Overview

This project implements a fully-connected Multilayer Perceptron (MLP) to classify images from the FashionMNIST dataset. The core objective was to conduct a rigorous comparative study between two distinct implementation approaches: an industry-standard Deep Learning framework (PyTorch) and a mathematically explicit implementation built solely on first principles (NumPy).

The goal was to demonstrate a deep, ground-up understanding of neural network mechanics, including backpropagation and complex optimizers, by successfully replicating the performance of an optimized framework.

## Key Features & Results

Both models used the same three-layer architecture ($\mathbf{784 \rightarrow 512 \rightarrow 256 \rightarrow 10}$), allowing for a fair comparison of implementation methods.

| Implementation | Core Technologies | Final Test Accuracy | Training Time |
| :--- | :--- | :--- | :--- |
| **PyTorch (Baseline)** | PyTorch, `torch.nn`, `torch.optim` | $88.92\%$ | $200.92$ seconds |
| **NumPy (From Scratch)** | NumPy, Python | $87.77\%$ | $293.61$ seconds |

### Advanced Algorithmic Implementation (NumPy)

The NumPy-only implementation required building all core components manually, showcasing expertise in numerical computation:

* **Custom Backpropagation:** Manually derived and implemented the full backward pass using NumPy, calculating gradients for all layers.
* **Adam Optimizer:** Implemented the full **Adam optimization algorithm** from scratch, including moment and velocity calculations with bias correction.
* **Batch Normalization:** Engineered the complete Batch Normalization layer, successfully implementing the complex forward and **backward passes** using raw linear algebra.
* **Regularization:** Integrated advanced regularization techniques, including **L2 Regularization**, **Dropout**, and **Label Smoothing**, directly into the custom cost and backward functions.

### Comparative Insights

* **Efficiency:** The NumPy implementation took significantly longer to train (almost twice as long) compared to PyTorch, highlighting the performance benefits of optimized C++ backends in modern frameworks.
* **Training Stability:** The NumPy model showed a slightly **smoother convergence** in its loss curves and exhibited **less overfitting** (smaller gap between training and test accuracy).

## Skills Used

| Category | Skills |
| :--- | :--- |
| **Deep Learning** | Multilayer Perceptrons (MLP), Backpropagation, Softmax, ReLU, Batch Normalization, Dropout, Label Smoothing. |
| **Programming/Tools** | Python, NumPy (Vectorization, Linear Algebra), PyTorch (API, `torch.nn`), Jupyter Notebooks, Matplotlib. |
| **Data Analysis** | Performance Benchmarking, Hyperparameter Tuning, Comparative Analysis. |

---
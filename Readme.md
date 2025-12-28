Hbb Jet Tagging using Machine Learning and Neural Networks

*Overview
This project addresses the **Hbb jet tagging** problem in **High Energy Physics (HEP)**, where the task is to classify jets originating from **H → b b̄ decays** against background jets using high-level jet features.

The project compares a classical machine learning baseline (**XGBoost**) with a **neural network (MLP)** and demonstrates a substantial performance improvement using deep learning.


Objective
- Build a binary classifier for Hbb jet identification
- Compare tree-based and neural network approaches
- Optimize performance using **ROC-AUC**, a standard metric in HEP



Dataset
- High-level engineered jet features (kinematic and substructure variables)
- Binary labels:
  - 1 → Hbb jet
  - 0 → Background jet
- Data split:
  - Training set
  - Validation set
  - Final test set (never used during training or tuning)


Models Implemented

1. XGBoost (Baseline)
- Gradient Boosted Decision Trees
- Hyperparameter tuning performed
- Serves as a strong classical ML baseline

Performance:
- ROC-AUC = 0.62


 2. Neural Network (MLP)
- Fully connected feedforward neural network
- Architecture:
  - Input layer
  - Multiple hidden layers with ReLU activation
  - Dropout regularization
  - Sigmoid output layer
- Loss function: Binary Cross-Entropy
- Optimizer: Adam

Performance:
- ROC-AUC =0.89

This represents a large improvement over XGBoost, highlighting the ability of neural networks to capture complex non-linear feature interactions present in jet substructure data.

---

 Results

| Model    | ROC-AUC |
|---------|---------|
| XGBoost | 0.62    |
| MLP     | 0.89    |


 Key Observations
- Tree-based models struggle with highly correlated and non-linear physics features
- Neural networks significantly outperform classical methods for this task
- Feature scaling and regularization play a critical role
- ROC-AUC is preferred over accuracy due to class imbalance

 Tech Stack
- Python
- NumPy, Pandas
- Scikit-learn
- XGBoost
- PyTorch (Neural Network)
- Matplotlib, Seaborn


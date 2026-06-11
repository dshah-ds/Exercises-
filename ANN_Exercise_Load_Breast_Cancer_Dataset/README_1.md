# 🧠 ANN_exercise_load_breast_dataset

> Hands-on exploration of Artificial Neural Networks using TensorFlow/Keras on a real-world medical dataset.

---

## 📋 Overview

This notebook walks through **8 progressive exercises** covering core ANN concepts — from data preparation all the way to deployment planning. The dataset used is the **Wisconsin Breast Cancer Diagnostic Dataset** (569 samples, 30 features, binary classification).

### 🎯 What You'll Learn
- Preparing medical tabular data for neural networks (scaling, splitting)
- Building and evaluating a baseline ANN in Keras
- Comparing loss functions: Binary Cross-Entropy vs MSE
- Comparing optimizers: SGD, Adam, RMSProp
- Understanding activation functions: ReLU vs Sigmoid in hidden layers
- Evaluating the impact of network depth on accuracy and overfitting
- Planning a model-to-production deployment pipeline

---

## 📁 Repository Structure

```
├── ANN_exercise_load_breast_dataset.ipynb   ← Main notebook (run this)
├── README.md                                        ← This file
└── requirements.txt                                 ← Python dependencies
```

---

## 🔬 Exercises at a Glance

| # | Exercise | Key Concept |
|---|---|---|
| 1 | Load & Explore Dataset | sklearn built-in datasets, class distribution |
| 2 | Train-Test Split | Stratification, reproducibility |
| 3 | Feature Scaling | StandardScaler, data leakage prevention |
| 4 | Baseline ANN | Keras Sequential, Binary Cross-Entropy, Adam |
| 5 | Loss: MSE vs Cross-Entropy | Why cross-entropy is correct for classification |
| 6 | Optimizers: SGD vs Adam vs RMSProp | Convergence speed, adaptive learning rates |
| 7 | Activations: ReLU vs Sigmoid (hidden) | Vanishing gradient problem |
| 8 | Depth: 1 vs 2 Hidden Layers | Overfitting detection, depth vs capacity |

---

## 🚀 Quick Start

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/ANN_exercise_load_breast_dataset.git
cd ANN_exercise_load_breast_dataset
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Launch Jupyter
```bash
jupyter notebook ANN_exercise_load_breast_dataset.ipynb
```

### Or open in Google Colab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/ANN_exercise_load_breast_dataset/blob/main/ANN_exercise_load_breast_dataset.ipynb)

---

## 📊 Key Results Summary

| Experiment | Test Accuracy | Note |
|---|---|---|
| Baseline ANN (16 neurons, ReLU, Adam) | ~97% | Strong baseline |
| MSE Loss (same arch) | ~96% | Slightly lower, theoretically wrong choice |
| SGD Optimizer | ~93–96% | Slower convergence at lr=0.01 |
| RMSProp Optimizer | ~96–97% | Comparable to Adam |
| Sigmoid Hidden Layer | ~95–97% | ReLU performs comparably on shallow net |
| 2 Hidden Layers | ~96–97% | Minimal gain on 569 samples |

---

## ⚠️ Key Takeaways (What to Keep in Mind)

1. **Always use `binary_crossentropy`** for binary classification — MSE is for regression.
2. **Never fit the scaler on test data** — this is data leakage.
3. **Adam is the default optimizer** for most deep learning tasks.
4. **ReLU is preferred in hidden layers** — Sigmoid causes vanishing gradients in deeper nets.
5. **More layers ≠ always better** — monitor the train-test accuracy gap for overfitting.
6. **Save both model AND scaler** when deploying — the scaler is part of the inference pipeline.

---

## 🗺️ Deployment Roadmap

```
Best Model → Save (.h5 / pickle) → Build REST API (Flask/FastAPI) → Containerize (Docker) → Host (Cloud)
```

See the final section of the notebook for a complete code walkthrough of each step.

---

## 🛠️ Tech Stack

| Library | Version | Purpose |
|---|---|---|
| Python | 3.9+ | Core language |
| TensorFlow / Keras | 2.x | Neural network framework |
| scikit-learn | 1.x | Dataset, preprocessing, splitting |
| NumPy | 1.x | Numerical operations |
| Pandas | 2.x | Data manipulation & display |

---

## 📚 References

- [Breast Cancer Wisconsin Dataset — scikit-learn docs](https://scikit-learn.org/stable/datasets/toy_dataset.html#breast-cancer-dataset)
- [Keras Sequential API](https://keras.io/guides/sequential_model/)
- [Understanding Binary Cross-Entropy](https://ml-cheatsheet.readthedocs.io/en/latest/loss_functions.html)
- [Adam Optimizer Paper — Kingma & Ba (2014)](https://arxiv.org/abs/1412.6980)

---
 
*Author: Devam Shah | [LinkedIn](www.linkedin.com/in/devam-a-shah)*

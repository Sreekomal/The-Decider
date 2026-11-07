# THE DECIDER
### Every prediction has a reason.

An interactive **Decision Tree Classification System** that implements ID3 and C4.5, allowing users to explore datasets, train classification models, compare performance, visualize decision trees, and understand individual predictions.

---

## Overview

THE DECIDER is a machine learning application developed to demonstrate and compare two fundamental decision tree algorithms: **ID3** and **C4.5**.

The application provides an end-to-end classification workflow, from uploading a dataset and preprocessing data to training models, evaluating performance, and inspecting how predictions are made.

The objective is to make decision tree classification **interactive, interpretable, and easy to explore**.

## Features

- **Dataset Explorer:** Upload CSV datasets, inspect data, and select the target attribute.
- **Data Preprocessing:** Handle missing values and prepare data for model training.
- **ID3 Classifier:** Custom implementation using Entropy and Information Gain.
- **C4.5 Classifier:** Custom implementation using Gain Ratio and numerical threshold-based splitting.
- **Model Comparison:** Compare ID3 and C4.5 using a common train-test split.
- **Decision Tree Explorer:** Interactive visualization with zoom, pan, search, and node inspection.
- **Prediction Interface:** Generate predictions from input data.
- **Reason Inspector:** Trace the decision path followed by a prediction.
- **Model Evaluation:** Evaluate performance using accuracy, precision, recall, F1-score, and confusion matrices.

## Algorithms

### ID3 — Iterative Dichotomiser 3

ID3 constructs a decision tree by selecting the feature with the highest Information Gain at each step.

- Uses Entropy to measure impurity.
- Uses Information Gain to select splitting features.
- Supports categorical multi-way splits.
- Numerical features are discretized before training.

### C4.5

C4.5 improves upon ID3 by using Gain Ratio and supporting numerical threshold-based splits.

- Uses Gain Ratio for split selection.
- Supports categorical and numerical features.
- Numerical features can be split using thresholds.
- Reduces the bias of Information Gain toward attributes with many distinct values.

| Aspect | ID3 | C4.5 |
|---|---|---|
| Split criterion | Information Gain | Gain Ratio |
| Numerical features | Discretized before training | Threshold-based splitting |
| Categorical features | Multi-way splits | Categorical splits |
| Tree construction | Recursive | Recursive |

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core implementation |
| Pandas | Dataset processing |
| NumPy | Numerical computation |
| Scikit-learn | Supporting preprocessing and evaluation utilities |
| Streamlit | Interactive web application |
| Matplotlib | Evaluation plots |
| Graphviz | Tree export and visualization support |
| D3.js | Interactive decision tree visualization |
| Pytest | Automated testing |

## Application Workflow

```text
Upload CSV Dataset
        ↓
Explore Dataset & Select Target
        ↓
Preprocessing
        ↓
Train-Test Split
        ↓
Train ID3 and C4.5
        ↓
Evaluate Models
        ↓
Compare Performance
        ↓
Explore Decision Trees
        ↓
Generate Predictions
        ↓
Inspect Prediction Reasoning
